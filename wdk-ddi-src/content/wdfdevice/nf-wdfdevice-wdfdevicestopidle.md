---
UID: NF:wdfdevice.WdfDeviceStopIdle
title: WdfDeviceStopIdle macro (wdfdevice.h)
description: The WdfDeviceStopIdle method informs the framework that the specified device must be placed in its working (D0) power state.
old-location: wdf\wdfdevicestopidle.htm
tech.root: wdf
ms.date: 08/11/2022
keywords: ["WdfDeviceStopIdle macro"]
ms.keywords: DFDeviceObjectGeneralRef_3dbde224-ecdf-429e-9389-9bdb49b16040.xml, WdfDeviceStopIdle, WdfDeviceStopIdle method, kmdf.wdfdevicestopidle, wdf.wdfdevicestopidle, wdfdevice/WdfDeviceStopIdle
req.header: wdfdevice.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (KMDF); WUDFx02000.dll (UMDF)
req.dll: 
req.irql: See Remarks section.
targetos: Windows
req.typenames: 
f1_keywords:
 - WdfDeviceStopIdle
 - wdfdevice/WdfDeviceStopIdle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Wdf01000.sys
 - Wdf01000.sys.dll
 - WUDFx02000.dll
 - WUDFx02000.dll.dll
api_name:
 - WdfDeviceStopIdle
---

# WdfDeviceStopIdle macro

## -description

**[Applies to KMDF and UMDF]**

The **WdfDeviceStopIdle** method informs the framework that the specified device must be placed in its working (D0) power state.

## -parameters

### -param Device [in]

A handle to a framework device object.

### -param WaitForD0 [in]

A Boolean value that indicates when **WdfDeviceStopIdle** will return. If **TRUE**, it returns only after the specified device has entered the D0 device power state. If **FALSE**, the method returns immediately.

## -syntax

```cpp
NTSTATUS WdfDeviceStopIdle(
   _In_ WDFDEVICE Device,
   _In_ BOOLEAN WaitForD0
);
```

## -remarks

This macro can return the following values:

| Return value | Meaning |
|--|--|
| STATUS_PENDING | The device is being powered up asynchronously. |
| STATUS_INVALID_DEVICE_STATE | The driver is not the power policy owner for the device. |
| STATUS_POWER_STATE_INVALID | A device failure occurred and the device cannot enter its D0 power state. |

The method might return other NTSTATUS values.

> [!NOTE]
> For devices that specify **SystemManagedIdleTimeout** or **SystemManagedIdleTimeoutWithHint** in the [WDF_POWER_POLICY_IDLE_TIMEOUT_TYPE](ne-wdfdevice-_wdf_power_policy_idle_timeout_type.md) enumeration, when calling **WdfDeviceStopIdle** with *WaitForD0* set to **FALSE**, if the device is still in D0 and the idle timeout period has not yet elapsed, starting in WDF versions 1.33/2.33, **WdfDeviceStopIdle** returns STATUS_SUCCESS (in previous versions this resulted in a return value of STATUS_PENDING).

A bug check occurs if the driver supplies an invalid object handle.

If your device can enter a low-power state when it becomes idle, your driver might have to occasionally call **WdfDeviceStopIdle** to bring the device back to its working (D0) state or to prevent it from entering a low-power state. 

**WdfDeviceStopIdle** does not prevent the framework from transitioning the device to a sleep state when the system changes to an Sx sleep state. Its only effect is to prevent transitions to Dx sleep states while the system is in the S0 working state. Similarly, if the device supports [directed power management](/windows-hardware/design/device-experiences/directed-power-management), **WdfDeviceStopIdle** does not prevent the device from entering directed power down.

> [!WARNING]
> Do not call **WdfDeviceStopIdle** with *WaitForD0* = **TRUE** during power down, either directly or indirectly. For example, if the **[EvtDeviceArmWakeFromS0](./nc-wdfdevice-evt_wdf_device_arm_wake_from_s0.md)** callback waits on another thread which calls `WdfDeviceStopIdle(TRUE)`, the power transition is blocked and the system crashes.

Your driver *does not* have to call **WdfDeviceStopIdle** when a device is idle and the framework places an I/O request in the device's power-managed I/O queue. Additionally, your driver *does not* have to call **WdfDeviceStopIdle** when a device is idle and it detects a wake signal. In both of these cases, the framework requests the bus driver to restore the device's power state to D0.

Although drivers typically do not need to call **WdfDeviceStopIdle** when handling I/O requests that they obtain from a power-managed I/O queue, the call is allowed. However, drivers must not set the *WaitForD0* parameter to **TRUE** when handling I/O requests from a power-managed I/O queue.

Your driver *does* have to call **WdfDeviceStopIdle** if it must access the device because of a request that the driver has received outside of a power-managed I/O queue. For example, your driver might support a driver-defined interface or a WMI request that requires accessing the device. In this case, you must ensure that the device is in its working state before the driver accesses the device, and that the device remains in its working state until the driver has finished accessing the device.

Calling **WdfDeviceStopIdle** forces the device into its working (D0) state, if the system is in its working (S0) state. The device remains in its working state until the driver calls [WdfDeviceResumeIdle](./nf-wdfdevice-wdfdeviceresumeidle.md), at which point the framework can place the device in a low-power state if it remains idle.

Do not call **WdfDeviceStopIdle** before the framework has called the driver's [EvtDeviceD0Entry](./nc-wdfdevice-evt_wdf_device_d0_entry.md) callback function for the first time.

A call to **WdfDeviceStopIdle** can restore an idle device to its working state only if the system is in its working (S0) state. If the system is transitioning to a low-power state or the device has already been powered down in response to Sx (where x > 0) when a driver calls **WdfDeviceStopIdle** with the *WaitForD0* parameter set to **TRUE**, the function does not return until the system returns to its S0 state.

Every successful call to **WdfDeviceStopIdle** must eventually be followed by a call to [WdfDeviceResumeIdle](./nf-wdfdevice-wdfdeviceresumeidle.md), or else the device will never return to a low-power state if it again becomes idle. Calls to **WdfDeviceStopIdle** can be nested, so the number of calls to **WdfDeviceResumeIdle** must equal the number of calls to **WdfDeviceStopIdle**.  Do not call **WdfDeviceResumeIdle** if a call to **WdfDeviceStopIdle** fails.

If the system enters a low-power state after **WdfDeviceStopIdle** returns, the device also enters a low-power state. When the system returns to its working (S0) state, the device also returns to its working (D0) state.  The power reference from the call to **WdfDeviceStopIdle** remains active and prevents the device from entering a low-power state until there is a matching call to  [WdfDeviceResumeIdle](./nf-wdfdevice-wdfdeviceresumeidle.md).

For more information, see [Supporting Idle Power-Down](/windows-hardware/drivers/wdf/supporting-idle-power-down).

If *WaitForD0* is **TRUE**, **WdfDeviceStopIdle** must be called at IRQL = PASSIVE_LEVEL. If *WaitForD0* is **FALSE**, this method must be called at IRQL <= DISPATCH_LEVEL.

Calling [WdfDeviceStopIdleWithTag](/windows-hardware/drivers/wdf/wdfdevicestopidlewithtag) instead of **WdfDeviceStopIdle** provides additional information (tag value, line number, and file name) that you can view in Microsoft debuggers.  

### Examples

In the following code example, **WdfDeviceStopIdle** returns after the specified device has entered the D0 device power state.

```cpp
NTSTATUS  status;

status = WdfDeviceStopIdle(Device, TRUE);
```

## -see-also

- [Debugging Power Reference Leaks in WDF](/windows-hardware/drivers/wdf/debugging-power-reference-leaks-in-wdf)
- [WdfDeviceResumeIdle](./nf-wdfdevice-wdfdeviceresumeidle.md)
- [WdfDeviceResumeIdleWithTag](/windows-hardware/drivers/wdf/wdfdeviceresumeidlewithtag)
- [WdfDeviceStopIdleWithTag](/windows-hardware/drivers/wdf/wdfdevicestopidlewithtag)
