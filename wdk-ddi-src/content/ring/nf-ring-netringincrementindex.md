---
UID: NF:ring.NetRingIncrementIndex
title: NetRingIncrementIndex function (ring.h)
description: Returns the next index value after the specified index value, wrapping around to the beginning of the ring buffer if necessary.
tech.root: netvista
ms.date: 12/10/2021
keywords: ["NetRingIncrementIndex function"]
ms.keywords: NetRingIncrementIndex
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
 - NetRingIncrementIndex
 - ring/NetRingIncrementIndex
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ring.h
api_name:
 - NetRingIncrementIndex
---

# NetRingIncrementIndex function


## -description

Returns the next index value after the specified index value, wrapping around to the beginning of the ring buffer if necessary.

## -parameters

### -param Ring [in]

A pointer to a [**NET_RING**](../ring/ns-ring-_net_ring.md).

### -param Index [in]

The index value to increment.

## -returns

Returns the next index value after the specified index value, wrapping around to the beginning of the ring buffer if necessary.

## -remarks

This routine is a convenient equivalent to calling [**NetRingAdvanceIndex**](../ring/nf-ring-netringadvanceindex.md) with a **Distance** of **1**.

## -see-also

[**NET_RING**](../ring/ns-ring-_net_ring.md)

[**NetRingAdvanceIndex**](../ring/nf-ring-netringadvanceindex.md)

