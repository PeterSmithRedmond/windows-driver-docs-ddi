---
UID: NF:netadapter.NetAdapterSetPermanentLinkLayerAddress
title: NetAdapterSetPermanentLinkLayerAddress function (netadapter.h)
description: The NetAdapterSetPermanentLinkLayerAddress function sets the permanent link layer address for the network adapter.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetAdapterSetPermanentLinkLayerAddress function"]
ms.keywords: NetAdapterSetPermanentLinkLayerAddress
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.23
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
req.alt-api: 
req.alt-loc: 
req.typenames: NetAdapterSetPermanentLinkLayerAddress
targetos: Windows
f1_keywords:
 - NetAdapterSetPermanentLinkLayerAddress
 - netadapter/NetAdapterSetPermanentLinkLayerAddress
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - NetAdapterSetPermanentLinkLayerAddress
---

# NetAdapterSetPermanentLinkLayerAddress function


## -description

The **NetAdapterSetPermanentLinkLayerAddress** function sets the permanent link layer address for the network adapter.

## -parameters

### -param Adapter [_In_]

The network adapter object that the client created in a prior call to [NetAdapterCreate](nf-netadapter-netadaptercreate.md).

### -param LinkLayerAddress [_In_]

A pointer to a driver-allocated allocated [NET_ADAPTER_LINK_LAYER_ADDRESS](ns-netadapter-net_adapter_link_layer_address.md) structure that the driver initialized in a prior call to [NET_ADAPTER_LINK_LAYER_ADDRESS_INIT](nf-netadapter-net_adapter_link_layer_address_init.md).

## -remarks

## -see-also

[NET_ADAPTER_LINK_LAYER_ADDRESS](ns-netadapter-net_adapter_link_layer_address.md)