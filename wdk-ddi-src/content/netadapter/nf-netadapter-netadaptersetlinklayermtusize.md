---
UID: NF:netadapter.NetAdapterSetLinkLayerMtuSize
title: NetAdapterSetLinkLayerMtuSize function (netadapter.h)
description: Sets the link layer maximum transfer unit size of the adapter.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetAdapterSetLinkLayerMtuSize function"]
ms.keywords: NetAdapterSetLinkLayerMtuSize
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.21
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
req.alt-api: 
req.alt-loc: 
req.typenames: NetAdapterSetLinkLayerMtuSize
targetos: Windows
f1_keywords:
 - NetAdapterSetLinkLayerMtuSize
 - netadapter/NetAdapterSetLinkLayerMtuSize
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - NetAdapterSetLinkLayerMtuSize
---

# NetAdapterSetLinkLayerMtuSize function


## -description

Sets the link layer maximum transfer unit size of the adapter.

## -parameters

### -param Adapter [_In_]

The network adapter object that the client created in a prior call to [**NetAdapterCreate**](nf-netadapter-netadaptercreate.md).

### -param MtuSize [_In_]

The new size of the adapter's MTU, in bytes.

## -remarks

The client driver first sets MTU size by calling **NetAdapterSetLinkLayerMtuSize** when starting a net adapter, before calling [**NetAdapterStart**](nf-netadapter-netadapterstart.md).

The client driver can change the MTU size after [**NetAdapterStart**](nf-netadapter-netadapterstart.md) returns by calling this function again. Doing so causes all of the adapter's transmit (Tx) and receive (Rx) queues to be recreated.

## -see-also

[NetAdapterSetLinkLayerCapabilities](nf-netadapter-netadaptersetlinklayercapabilities.md)

