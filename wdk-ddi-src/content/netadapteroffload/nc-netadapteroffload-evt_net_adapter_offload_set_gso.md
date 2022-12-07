---
UID: NC:netadapteroffload.EVT_NET_ADAPTER_OFFLOAD_SET_GSO
title: EVT_NET_ADAPTER_OFFLOAD_SET_GSO (netadapteroffload.h)
description: The EvtNetAdapterOffloadSetGso callback function is implemented by the client driver to set changes in TCP and UDP large send offload capabilities.
tech.root: netvista
ms.date: 10/09/2020
keywords: ["EVT_NET_ADAPTER_OFFLOAD_SET_GSO callback function"]
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
 - EVT_NET_ADAPTER_OFFLOAD_SET_GSO
 - netadapteroffload/EVT_NET_ADAPTER_OFFLOAD_SET_GSO
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - netadapteroffload.h
api_name:
 - EVT_NET_ADAPTER_OFFLOAD_SET_GSO
product:
 - Windows
---

# EVT_NET_ADAPTER_OFFLOAD_SET_GSO callback function


## -description


The client driver implements the *EvtNetAdapterOffloadSetGso* callback function to query changes in active Generic Segmentation Offload (GSO) capabilities and update the hardware settings accordingly.

## -parameters

### -param Adapter [_In_]

A handle to a NETADAPTER object the client driver previously created with a call to [**NetAdapterCreate**](../netadapter/nf-netadapter-netadaptercreate.md).

### -param Offload [_In_]

A handle to a NETOFFLOAD object that describes the adapter's offload capabilities.

## -remarks

Register your implementation of this callback function by setting the appropriate parameter when calling [**NetAdapterOffloadSetGsoCapabilities**](nf-netadapteroffload-netadapteroffloadsetgsocapabilities.md).

For an example implementation of this callback, see [Generic Segmentation Offload](/windows-hardware/drivers/netcx/gso-offload).

## -see-also

[Generic Segmentation Offload](/windows-hardware/drivers/netcx/gso-offload)

[**NET_ADAPTER_OFFLOAD_GSO_CAPABILITIES**](ns-netadapteroffload-_net_adapter_offload_gso_capabilities.md)

[**NetAdapterOffloadSetGsoCapabilities**](nf-netadapteroffload-netadapteroffloadsetgsocapabilities.md)

[**NET_ADAPTER_OFFLOAD_GSO_CAPABILITIES_INIT**](nf-netadapteroffload-net_adapter_offload_gso_capabilities_init.md)

