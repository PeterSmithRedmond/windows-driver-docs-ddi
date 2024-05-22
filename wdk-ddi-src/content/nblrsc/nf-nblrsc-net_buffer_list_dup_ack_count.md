---
UID: NF:nblrsc.NET_BUFFER_LIST_DUP_ACK_COUNT
title: NET_BUFFER_LIST_DUP_ACK_COUNT
ms.date: 11/30/2020
targetos: Windows
description: The NET_BUFFER_LIST_DUP_ACK_COUNT is a macro that NDIS drivers use to get and set the number of coalesced segments in a NET_BUFFER_LIST structure.
tech.root: netvista
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ndis/nblrsc.h
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
 - HeaderDef
api_location:
 - nblrsc.h
api_name:
 - NET_BUFFER_LIST_DUP_ACK_COUNT
f1_keywords:
 - NET_BUFFER_LIST_DUP_ACK_COUNT
 - nblrsc/NET_BUFFER_LIST_DUP_ACK_COUNT
dev_langs:
 - c++
---

# NET_BUFFER_LIST_DUP_ACK_COUNT macro


## -description

The **NET_BUFFER_LIST_DUP_ACK_COUNT** is a macro that NDIS drivers use to get and set the number of coalesced segments in a [**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md) structure.

## -parameters

### -param _NBL

A pointer to a **NET_BUFFER_LIST** structure.

## -returns

**NET_BUFFER_LIST_DUP_ACK_COUNT** returns the **DupAckCount** member of the [**NDIS_RSC_NBL_INFO**](../nblrsc/ns-nblrsc-ndis_rsc_nbl_info.md) union that is associated with the **TcpRecvSegCoalesceInfo** identifier. The information is retrieved from the **NetBufferListInfo** member of the indicated [**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md) structure.

## -remarks

This macro uses the [NET_BUFFER_LIST_INFO](../nblaccessors/nf-nblaccessors-net_buffer_list_info.md) macro to access the **TcpRecvSegCoalesceInfo** information.

## -see-also

[**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md)

[**NDIS_RSC_NBL_INFO**](../nblrsc/ns-nblrsc-ndis_rsc_nbl_info.md)

[NET_BUFFER_LIST_INFO](../nblaccessors/nf-nblaccessors-net_buffer_list_info.md)
