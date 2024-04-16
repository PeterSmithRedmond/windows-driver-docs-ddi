---
UID: NF:ufxclient.UfxDeviceIoInternalControl
title: UfxDeviceIoInternalControl function (ufxclient.h)
description: Passes kernel mode IOCTLs to UFX.
old-location: buses\ufxdeviceiointernalcontrol.htm
tech.root: usbref
ms.date: 01/20/2022
keywords: ["UfxDeviceIoInternalControl function"]
ms.keywords: UfxDeviceIoInternalControl, UfxDeviceIoInternalControl method [Buses], buses.ufxdeviceiointernalcontrol, ufxclient/UfxDeviceIoInternalControl
req.header: ufxclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ufxstub.lib
req.dll: 
req.irql: DISPATCH_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - UfxDeviceIoInternalControl
 - ufxclient/UfxDeviceIoInternalControl
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ufxclient.h
api_name:
 - UfxDeviceIoInternalControl
---

# UfxDeviceIoInternalControl function

## -description

Passes kernel mode IOCTLs to UFX.

## -parameters

### -param UfxDevice [in]

A handle to a UFX device object that the driver created by calling <a href="/windows-hardware/drivers/ddi/ufxclient/nf-ufxclient-ufxdevicecreate">UfxDeviceCreate</a>.

### -param Request [in]

A handle to a framework request object.

### -param OutputBufferLength [in]

The length, in bytes, of the request's output buffer, if an output buffer is available.

### -param InputBufferLength [in]

The length, in bytes, of the request's input buffer, if an input buffer is available.

### -param IoControlCode [in]

The driver-defined or system-defined IOCTL that is associated with the request.

## -returns

A Boolean value indicating if the call was successful.

## -remarks

The client driver calls **UfxDeviceIoInternalControl** to forward internal IOCTLs that it receives in its [EvtIoInternalDeviceControl](../wdfio/nc-wdfio-evt_wdf_io_queue_io_internal_device_control.md) callback function to UFX. The following example shows how:

```cpp
VOID
DefaultQueue_EvtIoInternalDeviceControl(
    _In_ WDFQUEUE Queue,
    _In_ WDFREQUEST Request,
    _In_ size_t OutputBufferLength,
    _In_ size_t InputBufferLength,
    _In_ ULONG IoControlCode
    )
/*++

Routine Description:

    EvtIoInternalDeviceControl handler for the default Queue

Arguments:

    Queue -  Handle to the framework queue object that is associated with the
             I/O request.

    Request - Handle to a framework request object.

    OutputBufferLength - Size of the output buffer in bytes

    InputBufferLength - Size of the input buffer in bytes

    IoControlCode - I/O control code.

--*/
{
    WDFDEVICE WdfDevice;
    PCONTROLLER_CONTEXT ControllerContext;
    BOOLEAN HandledbyUfx;   

    TraceEntry();

    TraceVerbose("InternalQueue 0x%p, Request 0x%p, OutputBufferLength %d, "
                  "InputBufferLength %d, IoControlCode %d",
                  Queue, Request, (int) OutputBufferLength, 
                  (int) InputBufferLength, IoControlCode);
    
    WdfDevice = WdfIoQueueGetDevice(Queue);
    ControllerContext = DeviceGetControllerContext(WdfDevice);

    HandledbyUfx = UfxDeviceIoInternalControl(
                        ControllerContext->UfxDevice,
                        Request,
                        OutputBufferLength,
                        InputBufferLength,
                        IoControlCode);

    if (!HandledbyUfx) {
        TraceError("Received an unsupported IOCTL");
        WdfRequestComplete(Request, STATUS_INVALID_DEVICE_REQUEST);
    }

    TraceExit();
}
```
