---
UID: NF:netadapter.NetAdapterSetLinkState
title: NetAdapterSetLinkState function (netadapter.h)
description: Sets the current link state of the of the network adapter.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetAdapterSetLinkState function"]
ms.keywords: NetAdapterSetLinkState
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.29
req.umdf-ver: 2.33 
req.lib: 
req.dll: 
req.irql: <= DISPATCH_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.alt-api: 
req.alt-loc: 
req.typenames: NetAdapterSetLinkState
targetos: Windows
f1_keywords:
 - NetAdapterSetLinkState
 - netadapter/NetAdapterSetLinkState
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - NetAdapterSetLinkState
---

# NetAdapterSetLinkState function


## -description

Sets the link state of the of the network adapter.

## -parameters

### -param Adapter [_In_]

The network adapter object that the client created in a prior call to [**NetAdapterCreate**](nf-netadapter-netadaptercreate.md).

### -param State [_In_]

A pointer to an allocated and initialized [**NET_ADAPTER_LINK_STATE**](ns-netadapter-_net_adapter_link_state.md) structure that describes the link state of the adapter.

## -remarks

The client driver calls **NetAdapterSetLinkState** when starting a net adapter, before it calls [**NetAdapterStart**](nf-netadapter-netadapterstart.md). It can also call this function later when it needs to change the current link state.

## -see-also

[**NET_ADAPTER_LINK_STATE_INIT**](nf-netadapter-net_adapter_link_state_init.md)

[**NET_ADAPTER_LINK_STATE_INIT_DISCONNECTED**](nf-netadapter-net_adapter_link_state_init_disconnected.md)

