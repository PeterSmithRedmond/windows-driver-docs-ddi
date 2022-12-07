---
UID: NF:netadapteroffload.NetOffloadIsTxChecksumIPv4Enabled
title: NetOffloadIsTxChecksumIPv4Enabled function (netadapteroffload.h)
description: The NetOffloadIsTxChecksumIPv4Enabled function determines whether a net adapter has Tx IPv4 checksum offload enabled.
tech.root: netvista
ms.date: 10/06/2020
keywords: ["NetOffloadIsTxChecksumIPv4Enabled function"]
ms.keywords: NetOffloadIsTxChecksumIPv4Enabled
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
 - NetOffloadIsTxChecksumIPv4Enabled
 - netadapteroffload/NetOffloadIsTxChecksumIPv4Enabled
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NetOffloadIsTxChecksumIPv4Enabled
product:
 - Windows
---

# NetOffloadIsTxChecksumIPv4Enabled function


## -description

The **NetOffloadIsTxChecksumIPv4Enabled** function determines whether a net adapter has Tx IPv4 checksum offload enabled.

## -parameters

### -param Offload [_In_]

A NETOFFLOAD object that represents the net adapter's Tx checksum capabilities.

## -returns

Returns **TRUE** if Tx IPv4 checksum offload is enabled. Otherwise, returns **FALSE**.

## -remarks

Client drivers typically call this function during their [*EvtNetAdapterOffloadSetTxChecksum*](../netadapteroffload/nc-netadapteroffload-evt_net_adapter_offload_set_tx_checksum.md) callback to test whether an updated set of active Tx checksum capabilities includes Tx IPv4 checksum offload.

## -see-also

[Checksum Offload](/windows-hardware/drivers/netcx/checksum-offload)

[*EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM*](../netadapteroffload/nc-netadapteroffload-evt_net_adapter_offload_set_tx_checksum.md)

