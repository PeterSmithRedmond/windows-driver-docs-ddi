---
UID: NF:netadapteroffload.NetOffloadIsTcpRscIPv4Enabled
title: NetOffloadIsTcpRscIPv4Enabled
ms.date: 10/15/2020
targetos: Windows
description: The NetOffloadIsTcpRscIPv4Enabled function determines whether a net adapter has RSC offload enabled for IPv4 packets.
tech.root: netvista
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: netadapteroffload.h
req.idl: 
req.include-header: netadaptercx.h
req.irql: PASSIVE_LEVEL
req.kmdf-ver: 
req.lib: netadaptercxstub.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: Windows Server 2022
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadapteroffload.h
api_name:
 - NetOffloadIsTcpRscIPv4Enabled
f1_keywords:
 - NetOffloadIsTcpRscIPv4Enabled
 - netadapteroffload/NetOffloadIsTcpRscIPv4Enabled
dev_langs:
 - c++
ms.custom: Fe
---

## -description

The **NetOffloadIsTcpRscIPv4Enabled** function determines whether a net adapter has RSC offload enabled for IPv4 packets.

## -parameters

### -param Offload [_In_]

A NETOFFLOAD object that represents the net adapter's RSC capabilities.

## -returns

Returns **TRUE** if RSC offload is enabled for IPv4 packets, or **FALSE** if it is not.

## -remarks

Client drivers typically call this function during their [*EvtNetAdapterOffloadSetRsc*](../netadapteroffload/nc-netadapteroffload-evt_net_adapter_offload_set_rsc.md) callback to test whether an updated set of active RSC capabilities includes RSC offload for IPv4 packets.

## -see-also

[Receive Segment Coalescing offload](/windows-hardware/drivers/netcx/rsc-offload)

[*EvtNetAdapterOffloadSetRsc*](nc-netadapteroffload-evt_net_adapter_offload_set_rsc.md)

