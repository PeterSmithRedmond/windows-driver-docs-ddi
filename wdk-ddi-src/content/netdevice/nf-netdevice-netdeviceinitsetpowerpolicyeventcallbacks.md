---
UID: NF:netdevice.NetDeviceInitSetPowerPolicyEventCallbacks
title: NetDeviceInitSetPowerPolicyEventCallbacks function (netdevice.h)
description: The NetDeviceInitSetPowerPolicyEventCallbacks function sets optional power policy event callbacks during device initialization for a client driver.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NetDeviceInitSetPowerPolicyEventCallbacks function"]
ms.keywords: NetDeviceInitSetPowerPolicyEventCallbacks
req.header: netdevice.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 2.33 
req.lib: netadaptercxstub.lib
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: Vb
f1_keywords:
 - NetDeviceInitSetPowerPolicyEventCallbacks
 - netdevice/NetDeviceInitSetPowerPolicyEventCallbacks
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NetDeviceInitSetPowerPolicyEventCallbacks
---

# NetDeviceInitSetPowerPolicyEventCallbacks function


## -description

The **NetDeviceInitSetPowerPolicyEventCallbacks** function sets optional power policy event callbacks during device initialization for a client driver.

## -parameters

### -param DeviceInit [_Inout_]

A pointer to a WDFDEVICE_INIT object that the client driver received in its [*EvtDriverDeviceAdd*](../wdfdriver/nc-wdfdriver-evt_wdf_driver_device_add.md) routine.

### -param Callbacks [_In_]

A pointer to a client driver allocated and initialized [**NET_DEVICE_POWER_POLICY_EVENT_CALLBACKS**](../netdevice/ns-netdevice-_net_device_power_policy_event_callbacks.md) structure.


## -remarks

Initialize the WDFDEVICE_INIT object by calling [**NetDeviceInitConfig**](../netdevice/nf-netdevice-netdeviceinitconfig.md) before calling this function. Initialize the [**NET_DEVICE_POWER_POLICY_EVENT_CALLBACKS**](../netdevice/ns-netdevice-_net_device_power_policy_event_callbacks.md) structure by calling [**NET_DEVICE_POWER_POLICY_EVENT_CALLBACKS_INIT**](../netdevice/nf-netdevice-net_device_power_policy_event_callbacks_init.md), then fill in pointers to the callbacks that your client driver implements.

## -see-also

[Configuring Power Management](/windows-hardware/drivers/netcx/configuring-power-management)

[**NET_DEVICE_POWER_POLICY_EVENT_CALLBACKS**](../netdevice/ns-netdevice-_net_device_power_policy_event_callbacks.md)
