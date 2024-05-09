---
UID: NF:netadapter.NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT
title: NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT function (netadapter.h)
description: The NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT function initializes a NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES structure.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT function"]
ms.keywords: NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT
req.header: netadapter.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.29
req.umdf-ver: 2.33 
req.lib: netadaptercxstub.lib
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT
 - netadapter/NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT
---

# NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT function


## -description

> [!NOTE]
> The **NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT** function is deprecated in NetAdapterCx 2.1 and later. For more information on current checksum offload functions, see [Checksum offload](/windows-hardware/drivers/netcx/checksum-offload).

The **NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES_INIT** function initializes a [**NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES**](ns-netadapter-_net_adapter_offload_checksum_capabilities.md) structure.

## -parameters

### -param ChecksumCapabilities [_Out_]

A pointer to a driver-allocated [**NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES**](ns-netadapter-_net_adapter_offload_checksum_capabilities.md) structure.

### -param IPv4 [_In_]

A flag specifying whether the hardware can calculate and validate IPv4 checksum.

### -param Tcp [_In_]

A flag specifying whether the hardware can calculate and validate TCP checksum.

### -param Udp [_In_]

A flag specifying whether the hardware can calculate and validate UDP checksum.

### -param EvtAdapterOffloadSetChecksum [_In_]

A pointer to the client driver's implementation of the [*EVT_NET_ADAPTER_OFFLOAD_SET_CHECKSUM*](nc-netadapter-evt_net_adapter_offload_set_checksum.md) callback function.

## -remarks

The [**NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES**](ns-netadapter-_net_adapter_offload_checksum_capabilities.md) structure initialized by this function is passed as a parameter to the [**NetAdapterOffloadSetChecksumCapabilities**](nf-netadapter-netadapteroffloadsetchecksumcapabilities.md) function.

## -see-also

[NetAdapterCx hardware offloads](/windows-hardware/drivers/netcx/introduction-to-hardware-offloads)

[**NET_ADAPTER_OFFLOAD_CHECKSUM_CAPABILITIES**](ns-netadapter-_net_adapter_offload_checksum_capabilities.md)
