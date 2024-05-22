---
UID: NF:netreceivescaling.NetAdapterSetReceiveScalingCapabilities
title: NetAdapterSetReceiveScalingCapabilities function (netreceivescaling.h)
description: The NetAdapterSetReceiveScalingCapabilities function sets a net adapter's receive side scaling (RSS) capabilities.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NetAdapterSetReceiveScalingCapabilities function"]
ms.keywords: NetAdapterSetReceiveScalingCapabilities
req.header: netreceivescaling.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.25
req.umdf-ver: 2.33 
req.lib: 
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
f1_keywords:
 - NetAdapterSetReceiveScalingCapabilities
 - netreceivescaling/NetAdapterSetReceiveScalingCapabilities
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - NetAdapterSetReceiveScalingCapabilities
---

# NetAdapterSetReceiveScalingCapabilities function


## -description

The **NetAdapterSetReceiveScalingCapabilities** function sets a net adapter's receive side scaling (RSS) capabilities.

## -parameters

### -param Adapter [_In_]

The **NETADAPTER** object the driver obtained in a previous call to [NetAdapterCreate](../netadapter/nf-netadapter-netadaptercreate.md).

### -param Capabilities [_In_]

A pointer to a driver-allocated and initialized [NET_ADAPTER_RECEIVE_SCALING_CAPABILITIES](ns-netreceivescaling-_net_adapter_receive_scaling_capabilities.md) structure.

## -remarks

The client driver must call this function when starting a net adapter, before calling [**NetAdapterStart**](../netadapter/nf-netadapter-netadapterstart.md).

## -see-also

[NET_ADAPTER_RECEIVE_SCALING_CAPABILITIES](ns-netreceivescaling-_net_adapter_receive_scaling_capabilities.md)

[NET_ADAPTER_RECEIVE_SCALING_CAPABILITIES_INIT](nf-netreceivescaling-net_adapter_receive_scaling_capabilities_init.md)

[NetAdapterCx Receive Side Scaling](/windows-hardware/drivers/netcx/netadaptercx-receive-side-scaling-rss-)
