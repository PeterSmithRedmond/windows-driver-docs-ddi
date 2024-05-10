---
UID: NF:nbluro.NET_BUFFER_LIST_IS_URO_SET
tech.root: netvista
title: NET_BUFFER_LIST_IS_URO_SET
ms.date: 01/18/2024
targetos: Windows
description: NET_BUFFER_LIST_IS_URO_SET returns whether the UDP RSC (URO) offload information is set for a NET_BUFFER_LIST structure.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ndis/nbluro.h
req.idl: 
req.include-header: ndis.h
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
returns-override: true
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nbluro.h
api_name:
 - NET_BUFFER_LIST_IS_URO_SET
f1_keywords:
 - NET_BUFFER_LIST_IS_URO_SET
 - nbluro/NET_BUFFER_LIST_IS_URO_SET
dev_langs:
 - c++
helpviewer_keywords:
 - NET_BUFFER_LIST_IS_URO_SET
---

## -description

The **NET_BUFFER_LIST_IS_URO_SET** macro returns whether the [UDP Receive Segment Coalescing Offload (URO)](/windows-hardware/drivers/network/udp-rsc-offload) offload information is set for a [**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md) structure.

## -parameters

### -param _NBL

A pointer to a **NET_BUFFER_LIST** structure.

## -returns

Returns a non-zero value if the URO feature is enabled for this NET_BUFFER_LIST.


## -remarks

## -see-also

[**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md)

[UDP Receive Segment Coalescing Offload (URO)](/windows-hardware/drivers/network/udp-rsc-offload)
