---
UID: NE:netadapter._NET_ADAPTER_PAUSE_FUNCTION_TYPE
title: NET_ADAPTER_PAUSE_FUNCTION_TYPE (netadapter.h)
description: The NET_ADAPTER_PAUSE_FUNCTION_TYPE enumeration specifies what IEEE 802.3 pause frames a net adapter supports.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_ADAPTER_PAUSE_FUNCTION_TYPE enumeration"]
ms.keywords: NET_ADAPTER_PAUSE_FUNCTION_TYPE, NET_ADAPTER_PAUSE_FUNCTION_TYPE,
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: 
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: NET_ADAPTER_PAUSE_FUNCTION_TYPE
targetos: Windows
ms.custom: Vb
f1_keywords:
 - _NET_ADAPTER_PAUSE_FUNCTION_TYPE
 - netadapter/_NET_ADAPTER_PAUSE_FUNCTION_TYPE
 - NET_ADAPTER_PAUSE_FUNCTION_TYPE
 - netadapter/NET_ADAPTER_PAUSE_FUNCTION_TYPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - _NET_ADAPTER_PAUSE_FUNCTION_TYPE
 - NET_ADAPTER_PAUSE_FUNCTION_TYPE
---

# NET_ADAPTER_PAUSE_FUNCTION_TYPE enumeration


## -description

The **NET_ADAPTER_PAUSE_FUNCTION_TYPE** enumeration specifies what IEEE 802.3 pause frames a net adapter supports.

## -enum-fields

### -field NetAdapterPauseFunctionTypeUnsupported:0 

Indicates that the adapter or link partner does not support pause frames.

### -field NetAdapterPauseFunctionTypeSendOnly:1 

Indicates that the adapter and link partner only support sending pause frames from the adapter to the link partner.

### -field NetAdapterPauseFunctionTypeReceiveOnly:2 

Indicates that the adapter and link partner only support sending pause frames from the link partner to the adapter.

### -field NetAdapterPauseFunctionTypeSendAndReceive:3 

Indicates that the adapter and link partner support sending and receiving pause frames in both transint and receive directions.

### -field NetAdapterPauseFunctionTypeUnknown:4 

Indicates that pause frame negotiation is in progress. The pause frame support that the link partner provides is unknown.

## -remarks

This enumeration is a member of the [**NET_ADAPTER_LINK_STATE**](../netadapter/ns-netadapter-_net_adapter_link_state.md) structure.

## -see-also

[**NET_ADAPTER_LINK_STATE**](../netadapter/ns-netadapter-_net_adapter_link_state.md)

