---
UID: NF:nblaccessors.NET_BUFFER_FIRST_MDL
title: NET_BUFFER_FIRST_MDL
ms.date: 10/02/2023
targetos: Windows
description: NET_BUFFER_FIRST_MDL is a macro that NDIS drivers use to get the first MDL in a NET_BUFFER structure.
tech.root: netvista 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ndis/nblaccessors.h
req.idl: 
req.include-header: ndis.h
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
req.target-type: Universal
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nblaccessors.h
api_name:
 - NET_BUFFER_FIRST_MDL
f1_keywords:
 - NET_BUFFER_FIRST_MDL
 - nblaccessors/NET_BUFFER_FIRST_MDL
dev_langs:
 - c++
---

# NET_BUFFER_FIRST_MDL macro


## -description

**NET_BUFFER_FIRST_MDL** is a macro that NDIS drivers use to get the first MDL in a [**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md) structure.

## -syntax

```cpp
#define NET_BUFFER_FIRST_MDL(_NB) ((_NB)->MdlChain)
```

## -parameters

### -param _NB

A pointer to a **NET_BUFFER** structure.

## -returns

**NET_BUFFER_FIRST_MDL** returns a pointer to the first MDL in a linked list of MDLs that is associated with the indicated [**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md) structure.

## -remarks

**NET_BUFFER_FIRST_MDL** gets the return value from the **MdlChain** member of the [**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md) structure.

## -see-also

[**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md)


