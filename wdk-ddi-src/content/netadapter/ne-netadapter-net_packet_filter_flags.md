---
UID: NE:netadapter._NET_PACKET_FILTER_FLAGS
tech.root: netvista
title: NET_PACKET_FILTER_FLAGS
ms.date: 03/30/2022
targetos: Windows
description: NET_PACKET_FILTER_FLAGS describe a network adapter's receive packet filters.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: netadapter.h
req.include-header: netadaptercx.h
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: Windows Server 2022
req.target-type: 
req.typenames: 
req.umdf-ver: 2.33 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - _NET_PACKET_FILTER_FLAGS
 - NET_PACKET_FILTER_FLAGS
f1_keywords:
 - _NET_PACKET_FILTER_FLAGS
 - netadapter/_NET_PACKET_FILTER_FLAGS
 - NET_PACKET_FILTER_FLAGS
 - netadapter/NET_PACKET_FILTER_FLAGS
dev_langs:
 - c++
---

## -description

The **NET_PACKET_FILTER_FLAGS** enumeration describes a network adapter's receive packet filters.

## -enum-fields

### -field NetPacketFilterFlagDirected:0x00000001

The network adapter can filter directed packets. Directed packets contain a destination address equal to the MAC address of the NIC.

### -field NetPacketFilterFlagMulticast:0x00000002

The network adapter can filter multicast packets whose destination MAC address matches an address in the multicast address list.

### -field NetPacketFilterFlagAllMulticast:0x00000004

The network adapter can filter all multicast address packets, not just the ones enumerated in the multicast address list.

### -field NetPacketFilterFlagBroadcast:0x00000008

The network adapter can filter broadcast packets.

### -field NetPacketFilterFlagPromiscuous:0x00000020

The network adapter can filter all packets regardless of whether VLAN filtering is enabled or not and whether the VLAN identifier matches or not.

## -remarks

The driver uses the **NET_PACKET_FILTER_FLAGS** enumeration to specify the net adapter's receive packet filters in the [**NET_ADAPTER_RECEIVE_FILTER_CAPABILITIES**](ns-netadapter-net_adapter_receive_filter_capabilities.md) structure.

An initialized [**NET_ADAPTER_RECEIVE_FILTER_CAPABILITIES**](ns-netadapter-net_adapter_receive_filter_capabilities.md) structure is an input to [**NetAdapterSetReceiveFilterCapabilities**](nf-netadapter-netadaptersetreceivefiltercapabilities.md).

## -see-also

[**NET_ADAPTER_RECEIVE_FILTER_CAPABILITIES**](ns-netadapter-net_adapter_receive_filter_capabilities.md)

[*EVT_NET_ADAPTER_SET_RECEIVE_FILTER*](nc-netadapter-evt_net_adapter_set_receive_filter.md)

[**NET_ADAPTER_RECEIVE_FILTER_CAPABILITIES_INIT**](nf-netadapter-net_adapter_receive_filter_capabilities_init.md)

[**NetAdapterSetReceiveFilterCapabilities**](nf-netadapter-netadaptersetreceivefiltercapabilities.md)

[**NetReceiveFilterGetPacketFilter**](nf-netadapter-netreceivefiltergetpacketfilter.md)
