---
UID: NF:netadapteroffload.NetOffloadIsRxChecksumUdpEnabled
title: NetOffloadIsRxChecksumUdpEnabled function (netadapteroffload.h)
description: The NetOffloadIsRxChecksumUdpEnabled function determines whether a net adapter has Rx UDP checksum offload enabled.
tech.root: netvista
ms.date: 10/06/2020
keywords: ["NetOffloadIsRxChecksumUdpEnabled function"]
ms.keywords: NetOffloadIsRxChecksumUdpEnabled
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
 - NetOffloadIsRxChecksumUdpEnabled
 - netadapteroffload/NetOffloadIsRxChecksumUdpEnabled
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NetOffloadIsRxChecksumUdpEnabled
product:
 - Windows
---

# NetOffloadIsRxChecksumUdpEnabled function


## -description

The **NetOffloadIsRxChecksumUdpEnabled** function determines whether a net adapter has Rx UDP checksum offload enabled.

## -parameters

### -param Offload [_In_]

A NETOFFLOAD object that represents the net adapter's Rx checksum capabilities.

## -returns

Returns **TRUE** if Rx UDP checksum offload is enabled. Otherwise, returns **FALSE**.

## -remarks

Client drivers typically call this function during their [*EvtNetAdapterOffloadSetRxChecksum*](../netadapteroffload/nc-netadapteroffload-evt_net_adapter_offload_set_rx_checksum.md) callback to test whether an updated set of active Rx checksum capabilities includes Rx UDP checksum offload.

## -see-also

[Checksum Offload](/windows-hardware/drivers/netcx/checksum-offload)

[*EVT_NET_ADAPTER_OFFLOAD_SET_RX_CHECKSUM*](../netadapteroffload/nc-netadapteroffload-evt_net_adapter_offload_set_rx_checksum.md)

