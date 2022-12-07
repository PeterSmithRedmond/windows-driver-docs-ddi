---
UID: NF:netadapteroffload.NetOffloadIsRxChecksumIPv4Enabled
title: NetOffloadIsRxChecksumIPv4Enabled function (netadapteroffload.h)
description: The NetOffloadIsRxChecksumIPv4Enabled function determines whether a net adapter has Rx IPv4 checksum offload enabled.
tech.root: netvista
ms.date: 10/06/2020
keywords: ["NetOffloadIsRxChecksumIPv4Enabled function"]
ms.keywords: NetOffloadIsRxChecksumIPv4Enabled
req.header: netadapteroffload.h
req.include-header: netadaptercx.h
req.target-type: 
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: Windows Server 2022
req.kmdf-ver: 1.29
req.umdf-ver: 
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
f1_keywords:
 - NetOffloadIsRxChecksumIPv4Enabled
 - netadapteroffload/NetOffloadIsRxChecksumIPv4Enabled
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NetOffloadIsRxChecksumIPv4Enabled
product:
 - Windows
---

# NetOffloadIsRxChecksumIPv4Enabled function


## -description

The **NetOffloadIsRxChecksumIPv4Enabled** function determines whether a net adapter has Rx IPv4 checksum offload enabled.

## -parameters

### -param Offload [_In_]

A NETOFFLOAD object that represents the net adapter's Rx checksum capabilities.

## -returns

Returns **TRUE** if Rx IPv4 checksum offload is enabled. Otherwise, returns **FALSE**.

## -remarks

Client drivers typically call this function during their [*EvtNetAdapterOffloadSetRxChecksum*](../netadapteroffload/nc-netadapteroffload-evt_net_adapter_offload_set_rx_checksum.md) callback to test whether an updated set of active Rx checksum capabilities includes Rx IPv4 checksum offload.

## -see-also

[Checksum Offload](/windows-hardware/drivers/netcx/checksum-offload)

[*EVT_NET_ADAPTER_OFFLOAD_SET_RX_CHECKSUM*](../netadapteroffload/nc-netadapteroffload-evt_net_adapter_offload_set_rx_checksum.md)

