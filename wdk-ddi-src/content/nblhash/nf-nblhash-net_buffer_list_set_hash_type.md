---
UID: NF:nblhash.NET_BUFFER_LIST_SET_HASH_TYPE
title: NET_BUFFER_LIST_SET_HASH_TYPE
ms.date: 11/30/2020
targetos: Windows
description: The NET_BUFFER_LIST_SET_HASH_TYPE macro sets the hash type information in a NET_BUFFER_LIST structure.
tech.root: netvista
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ndis/nblhash.h
req.idl: 
req.include-header: ndis.h
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Supported in NDIS 6.30 and later.
req.target-min-winversvr: 
req.target-type: Universal
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
returns-override: true
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - nblhash.h
api_name:
 - NET_BUFFER_LIST_SET_HASH_TYPE
f1_keywords:
 - NET_BUFFER_LIST_SET_HASH_TYPE
 - nblhash/NET_BUFFER_LIST_SET_HASH_TYPE
dev_langs:
 - c++
---

# NET_BUFFER_LIST_SET_HASH_TYPE function


## -description

The **NET_BUFFER_LIST_SET_HASH_TYPE** macro sets the hash type information in a [**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md) structure.

## -parameters

### -param Nbl

A pointer to a **NET_BUFFER_LIST** structure.

### -param HashType

The hash type.

The hash type is an OR value of valid combinations of the following flags:

- NDIS_HASH_IPV4
- NDIS_HASH_TCP_IPV4
- NDIS_HASH_IPV6
- NDIS_HASH_TCP_IPV6
- NDIS_HASH_IPV6_EX
- NDIS_HASH_TCP_IPV6_EX

For more information about hash types and the valid combinations of these flags, see [RSS Hashing Types](/windows-hardware/drivers/network/rss-hashing-types).

## -remarks

A NIC (or its miniport driver) uses the receive side scaling (RSS) hash type to identify the portion of received network data that is used to calculate an RSS hash value.

For more information about the hash type, see [RSS Hashing Types](/windows-hardware/drivers/network/rss-hashing-types).

## -see-also

[**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md)

