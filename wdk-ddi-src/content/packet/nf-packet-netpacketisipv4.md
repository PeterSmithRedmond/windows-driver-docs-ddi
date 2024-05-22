---
UID: NF:packet.NetPacketIsIpv4
title: NetPacketIsIpv4 function (packet.h)
description: The NetPacketIsIpv4 function determines if a NET_PACKET is an IPv4 packet. This function is reserved for system use. Do not call this function from your code.
tech.root: netvista
ms.date: 01/30/2019
keywords: ["NetPacketIsIpv4 function"]
ms.keywords: NetPacketIsIpv4
req.header: packet.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.29
req.umdf-ver: 2.33 
req.lib: 
req.dll: 
req.irql: Any level as long as target memory is resident
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - NetPacketIsIpv4
 - packet/NetPacketIsIpv4
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - NetPacketIsIpv4
---

# NetPacketIsIpv4 function


## -description

The **NetPacketIsIpv4** function determines if a [**NET_PACKET**](ns-packet-_net_packet.md) is an IPv4 packet. 

>[!WARNING]
> This function is reserved for system use. Do not call this function from your code.

## -parameters

### -param packet

A pointer to a [**NET_PACKET**](ns-packet-_net_packet.md) structure.

## -returns

Returns **TRUE** if the packet is an IPv4 packet; false otherwise.

## -remarks

## -see-also

