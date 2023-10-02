---
UID: NF:nblaccessors.NET_BUFFER_DATA_PHYSICAL_ADDRESS
title: NET_BUFFER_DATA_PHYSICAL_ADDRESS
ms.date: 10/02/2023
targetos: Windows
description: The NET_BUFFER_DATA_PHYSICAL_ADDRESS macro retrieves the DataPhysicalAddress member of a NET_BUFFER structure.
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
req.target-min-winverclnt: Supported in NDIS 6.1 and later.
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
 - NET_BUFFER_DATA_PHYSICAL_ADDRESS
f1_keywords:
 - NET_BUFFER_DATA_PHYSICAL_ADDRESS
 - nblaccessors/NET_BUFFER_DATA_PHYSICAL_ADDRESS
dev_langs:
 - c++
---

# NET_BUFFER_DATA_PHYSICAL_ADDRESS macro


## -description

The **NET_BUFFER_DATA_PHYSICAL_ADDRESS** macro retrieves the **DataPhysicalAddress** member of a [**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md) structure.

## -syntax

```cpp
#define NET_BUFFER_DATA_PHYSICAL_ADDRESS(_NB) ((_NB)->DataPhysicalAddress)
```

## -parameters

### -param _NB

A pointer to a **NET_BUFFER** structure.

## -returns

**NET_BUFFER_DATA_PHYSICAL_ADDRESS** returns the **DataPhysicalAddress** member of a [**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md) structure.

## -remarks

NDIS network drivers should use the **NET_BUFFER_DATA_PHYSICAL_ADDRESS** macro to get the **DataPhysicalAddress** member of a [**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md) structure.

## -see-also

[**NET_BUFFER**](../nbl/ns-nbl-net_buffer.md)


