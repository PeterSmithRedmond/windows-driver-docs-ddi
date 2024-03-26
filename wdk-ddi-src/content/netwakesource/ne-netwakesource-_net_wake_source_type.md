---
UID: NE:netwakesource._NET_WAKE_SOURCE_TYPE
tech.root: netvista
title: NET_WAKE_SOURCE_TYPE
ms.date: 09/07/2022
targetos: Windows
description: The NET_WAKE_SOURCE_TYPE enumeration specifies the type of a wake-on-LAN (WoL) wake-up event for a net adapter.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: netwakesource.h
req.include-header: netadaptercx.h
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.target-type: 
req.typenames: NET_WAKE_SOURCE_TYPE
req.umdf-ver: 2.33 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netwakesource.h
api_name:
 - _NET_WAKE_SOURCE_TYPE
 - NET_WAKE_SOURCE_TYPE
f1_keywords:
 - _NET_WAKE_SOURCE_TYPE
 - netwakesource/_NET_WAKE_SOURCE_TYPE
 - NET_WAKE_SOURCE_TYPE
 - netwakesource/NET_WAKE_SOURCE_TYPE
dev_langs:
 - c++
---

## -description

The **NET_WAKE_SOURCE_TYPE** enumeration specifies the type for the source of a wake-on-LAN (WoL) wake-up event from a net adapter.

## -enum-fields

### -field NetWakeSourceTypeBitmapPattern:1 

The wake source is a bitmap pattern.

### -field NetWakeSourceTypeMagicPacket:2

The wake source is a magic packet, which is a special packet that contains 16 contiguous copies of the receiving net adapter's Ethernet address.

### -field NetWakeSourceTypeMediaChange:3

The wake source is a media connect or disconnect event.

### -field NetWakeSourceTypePacketFilterMatch:4

The wake source is a packet that matches a filter the driver supports, such as an Ethernet unicast frame.

### -field NetWakeSourceTypeEapolPacket:5

The wake source is an EAP over LAN (EAPOL) request identifier message.

## -remarks

Call [**NetWakeSourceGetType**](../netwakesource/nf-netwakesource-netwakesourcegettype.md) to get the type for a WoL source.

## -see-also

[Configuring power management](/windows-hardware/drivers/netcx/configuring-power-management)

[**NetWakeSourceGetType**](../netwakesource/nf-netwakesource-netwakesourcegettype.md)

