---
UID: NE:checksumtypes._NET_PACKET_TX_CHECKSUM_ACTION
title: NET_PACKET_TX_CHECKSUM_ACTION (checksumtypes.h)
description: The NET_PACKET_TX_CHECKSUM_ACTION enumeration specifies checksum action flags for a NET_PACKET_CHECKSUM structure during packet transmission.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_PACKET_TX_CHECKSUM_ACTION enumeration"]
ms.keywords: NET_PACKET_TX_CHECKSUM_ACTION, NET_PACKET_TX_CHECKSUM_ACTION,
req.header: checksumtypes.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 2.33 
req.ddi-compliance: 
req.max-support: 
req.typenames: NET_PACKET_TX_CHECKSUM_ACTION
targetos: Windows
ms.custom: Vb
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - checksumtypes.h
api_name:
 - _NET_PACKET_TX_CHECKSUM_ACTION
 - NET_PACKET_TX_CHECKSUM_ACTION
f1_keywords:
 - _NET_PACKET_TX_CHECKSUM_ACTION
 - checksumtypes/_NET_PACKET_TX_CHECKSUM_ACTION
 - NET_PACKET_TX_CHECKSUM_ACTION
 - checksumtypes/NET_PACKET_TX_CHECKSUM_ACTION
---

# NET_PACKET_TX_CHECKSUM_ACTION enumeration


## -description

The **NET_PACKET_TX_CHECKSUM_ACTION** enumeration specifies checksum action flags for a [**NET_PACKET_CHECKSUM**](../checksumtypes/ns-checksumtypes-_net_packet_checksum.md) structure during packet transmission.

## -enum-fields

### -field NetPacketTxChecksumActionPassthrough:0 

Indicates the client should not perform checksum calculation for this layer.

### -field NetPacketTxChecksumActionRequired:2 

Indicates the client should perform checksum calculation for this layer.

## -remarks

## -see-also

[**NET_PACKET_CHECKSUM**](../checksumtypes/ns-checksumtypes-_net_packet_checksum.md)

