---
UID: NC:netadapteroffload.EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM
title: EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM (netadapteroffload.h)
description: The client driver implements the EvtNetAdapterOffloadSetTxChecksum callback function to set changes in Tx checksum offload capabilities.
tech.root: netvista
ms.date: 10/06/2020
keywords: ["EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM callback function"]
req.header: netadapteroffload.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: Windows Server 2022
req.kmdf-ver: 1.29
req.umdf-ver: 
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
ms.custom: Fe
f1_keywords:
 - EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM
 - netadapteroffload/EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - netadapteroffload.h
api_name:
 - EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM
product:
 - Windows
---

# EVT_NET_ADAPTER_OFFLOAD_SET_TX_CHECKSUM callback function


## -description

The client driver implements the *EvtNetAdapterOffloadSetTxChecksum* callback function to query changes in active Tx checksum offload capabilities and update the hardware settings accordingly.

## -parameters

### -param Adapter [_In_]

A handle to a NETADAPTER object the client driver previously created with a call to [**NetAdapterCreate**](../netadapter/nf-netadapter-netadaptercreate.md).

### -param Offload [_In_]

A handle to a NETOFFLOAD object that describes the adapter's offload capabilities.

## -remarks

Register your implementation of this callback function by setting the appropriate parameter when calling [**NetAdapterOffloadSetTxChecksumCapabilities**](nf-netadapteroffload-netadapteroffloadsettxchecksumcapabilities.md).

For an example implementation of this callback, see [Checksum Offload](/windows-hardware/drivers/netcx/checksum-offload).

## -see-also

[Checksum Offload](/windows-hardware/drivers/netcx/checksum-offload)

[**NET_ADAPTER_OFFLOAD_TX_CHECKSUM_CAPABILITIES**](ns-netadapteroffload-_net_adapter_offload_tx_checksum_capabilities.md)

[**NetAdapterOffloadSetTxChecksumCapabilities**](nf-netadapteroffload-netadapteroffloadsettxchecksumcapabilities.md)

