---
UID: NS:packet._NET_PACKET
title: _NET_PACKET (packet.h)
description: Represents a single network packet.
tech.root: netvista
ms.date: 01/30/2019
keywords: ["NET_PACKET structure"]
ms.keywords: _NET_PACKET, NET_PACKET, *PNET_PACKET,
req.header: packet.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.29
req.umdf-ver: 2.33 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.alt-api: 
req.alt-loc: 
req.typenames: NET_PACKET, *PNET_PACKET
targetos: Windows
f1_keywords:
 - _NET_PACKET
 - packet/_NET_PACKET
 - NET_PACKET
 - packet/NET_PACKET
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - packet.h
api_name:
 - _NET_PACKET
 - NET_PACKET
---

# _NET_PACKET structure


## -description

Represents a single network packet.

## -struct-fields

### -field FragmentIndex

The index in the fragment ring of the first [**NET_FRAGMENT**](../fragment/ns-fragment-_net_fragment.md) structure in this packet's payload.

### -field FragmentCount

The number of [**NET_FRAGMENT**](../fragment/ns-fragment-_net_fragment.md) structures that belong to this packet.

### -field Layout

A [**NET_PACKET_LAYOUT**](ns-packet-_net_packet_layout.md) structure.

For transmit queues, if the host stack has enabled a task offload that uses a protocol header, specifies a read-only offset to each protocol field. For example, if TCP checksum offload is enabled, this member specifies the offset to the TCP header. Otherwise, this member is empty.

For receive queues, if the host stack has enabled a task offload that uses a protocol header, set the **Layer2Type**, **Layer3Type**, and **Layer4Type** flags. When there are no task offloads this member is empty.

### -field Ignore

For receive queues, the client sets this field to prevent the packet from being indicated to the host. For example, if the hardware encountered a DMA error while writing bytes into this the data buffer for this packet's fragments, the client can set this field to drop the partial packet.

For transmit queues, this field is read-only. If set, it indicates that the client should not transmit the packet.

### -field Scratch

A bit field value that the client may use for any purpose. When the **NET_PACKET** is reused, this value is reset to zero.

### -field Reserved1

Reserved. Client drivers must not read or write this value.

## -remarks

Each **NET_PACKET** structure represents a single network frame and contains basic metadata applicable to all packets, such as the framing layout. A **NET_PACKET** contains at least one [**NET_FRAGMENT**](../fragment/ns-fragment-_net_fragment.md) that describes the location in system memory where the packet data resides.

The **NET_PACKET** structure can be an element in a [**NET_RING**](../ring/ns-ring-_net_ring.md) structure.

## -see-also

