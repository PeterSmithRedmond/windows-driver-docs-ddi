---
UID: NF:netadapter.NetAdapterPowerOffloadSetNSCapabilities
title: NetAdapterPowerOffloadSetNSCapabilities function (netadapter.h)
description: The NetAdapterPowerOffloadSetNsCapabilities function sets a net adapter's capabilities for IPv6 Neighbor Solicitation (NS) low power protocol offload.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetAdapterPowerOffloadSetNSCapabilities function"]
ms.keywords: NetAdapterPowerOffloadSetNSCapabilities
req.header: netadapter.h
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
 - NetAdapterPowerOffloadSetNSCapabilities
 - netadapter/NetAdapterPowerOffloadSetNSCapabilities
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NetAdapterPowerOffloadSetNSCapabilities
---

# NetAdapterPowerOffloadSetNSCapabilities function


## -description

The **NetAdapterPowerOffloadSetNsCapabilities** function sets a net adapter's capabilities for IPv6 Neighbor Solicitation (NS) low power protocol offload.

## -parameters

### -param Adapter [_In_]

A handle to a NETADAPTER object that the client driver obtained from a previous call to [**NetAdapterCreate**](../netadapter/nf-netadapter-netadaptercreate.md).

### -param Capabilities [_In_]

A pointer to a client driver-allocated and initialized [**NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_power_offload_ns_capabilities.md) structure.

## -remarks

Client drivers typically call this function from within their [*EvtDevicePrepareHardware*](../wdfdevice/nc-wdfdevice-evt_wdf_device_prepare_hardware.md) callback, but **must** call this function before calling [**NetAdapterStart**](nf-netadapter-netadapterstart.md).

## -see-also

[Configuring power management](/windows-hardware/drivers/netcx/configuring-power-management)

[**NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES**](../netadapter/ns-netadapter-_net_adapter_power_offload_ns_capabilities.md)

[**NET_ADAPTER_POWER_OFFLOAD_NS_CAPABILITIES_INIT**](../netadapter/nf-netadapter-net_adapter_power_offload_ns_capabilities_init.md)

[**NetAdapterCreate**](../netadapter/nf-netadapter-netadaptercreate.md)

[*EvtDevicePrepareHardware*](../wdfdevice/nc-wdfdevice-evt_wdf_device_prepare_hardware.md)

[**NetAdapterStart**](nf-netadapter-netadapterstart.md)
