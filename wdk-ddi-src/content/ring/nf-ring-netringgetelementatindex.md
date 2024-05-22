---
UID: NF:ring.NetRingGetElementAtIndex
title: NetRingGetElementAtIndex function (ring.h)
description: The NetRingGetElementAtIndex function retrieves an element from a net ring.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NetRingGetElementAtIndex function"]
ms.keywords: NetRingGetElementAtIndex
req.header: ring.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.29
req.umdf-ver: 2.33 
req.lib: 
req.dll: 
req.irql: Any level as long as target memory is resident
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.alt-api: 
req.alt-loc: 
targetos: Windows
f1_keywords:
 - NetRingGetElementAtIndex
 - ring/NetRingGetElementAtIndex
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ring.h
api_name:
 - NetRingGetElementAtIndex
---

# NetRingGetElementAtIndex function


## -description

The **NetRingGetElementAtIndex** function retrieves an element from a net ring.

## -parameters

### -param Ring [_In_]

A pointer to a [**NET_RING**](../ring/ns-ring-_net_ring.md).

### -param Index [_In_]

The element index, within the range **[0, Ring->NumberOfElements)**.

## -returns

Returns the element at the specified location.

## -remarks

**NetRingGetElementAtIndex** uses the **ElementStride** member of the net ring to index into the buffer and returns the location of the specified element.

**NetRingGetElementAtIndex** is meant for generic use of net rings. Instead, a NetAdapterCx client driver typically calls either [**NetRingGetPacketAtIndex**](../ring/nf-ring-netringgetpacketatindex.md) for a packet ring or [**NetRingGetFragmentAtIndex**](../ring/nf-ring-netringgetfragmentatindex.md) for a fragment ring.

## -see-also

[**NetRingGetPacketAtIndex**](../ring/nf-ring-netringgetpacketatindex.md)

[**NetRingGetFragmentAtIndex**](../ring/nf-ring-netringgetfragmentatindex.md)

