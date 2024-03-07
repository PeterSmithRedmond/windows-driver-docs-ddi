---
UID: NE:extension._NET_EXTENSION_TYPE
title: NET_EXTENSION_TYPE (extension.h)
description: The NET_EXTENSION_TYPE enumeration specifies the type of extension that a client driver is querying.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_EXTENSION_TYPE enumeration"]
ms.keywords: NET_EXTENSION_TYPE, NET_EXTENSION_TYPE,
req.header: extension.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: NET_EXTENSION_TYPE
targetos: Windows
ms.custom: Vb
f1_keywords:
 - _NET_EXTENSION_TYPE
 - extension/_NET_EXTENSION_TYPE
 - NET_EXTENSION_TYPE
 - extension/NET_EXTENSION_TYPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - extension.h
api_name:
 - _NET_EXTENSION_TYPE
 - NET_EXTENSION_TYPE
---

# NET_EXTENSION_TYPE enumeration


## -description

The **NET_EXTENSION_TYPE** enumeration specifies the type of extension that a client driver is querying.

## -enum-fields

### -field NetExtensionTypePacket:1 

The extension is a [**NET_PACKET**](../packet/ns-packet-_net_packet.md) extension.

### -field NetExtensionTypeFragment:2 

The extension is a [**NET_FRAGMENT**](../fragment/ns-fragment-_net_fragment.md) extension.

### -field NetExtensionTypeBuffer
Reserved for system use.

## -remarks

Client drivers pass this enumeration as a value to [**NET_EXTENSION_QUERY_INIT**](../netadapterpacket/nf-netadapterpacket-net_extension_query_init.md) to differentiate between packet extensions and fragment extension queries during packet queue creation.

## -see-also

[Packet descriptors and extensions](/windows-hardware/drivers/netcx/packet-descriptors-and-extensions)

[**NET_PACKET**](../packet/ns-packet-_net_packet.md)

[**NET_FRAGMENT**](../fragment/ns-fragment-_net_fragment.md)

[**NET_EXTENSION_QUERY_INIT**](../netadapterpacket/nf-netadapterpacket-net_extension_query_init.md)

