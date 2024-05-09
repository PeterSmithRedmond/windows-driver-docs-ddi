---
UID: NF:extension.NetExtensionGetData
title: NetExtensionGetData function (extension.h)
description: The NetExtensionGetData function retrieves packet extension data for a net packet.
tech.root: netvista
ms.date: 02/06/2019
keywords: ["NetExtensionGetData function"]
ms.keywords: NetExtensionGetData
req.header: extension.h
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
 - NetExtensionGetData
 - extension/NetExtensionGetData
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - NetExtensionGetData
---

# NetExtensionGetData function


## -description

The **NetExtensionGetData** function retrieves packet extension data for a net packet.

## -parameters

### -param Extension

A pointer to a [**NET_EXTENSION**](../extension/ns-extension-_net_extension.md) structure that describes the requested extension information for this packet queue.

### -param Index

The index in the packet ring for the target [**NET_PACKET**](../packet/ns-packet-_net_packet.md).

## -returns

Returns a pointer to the structure that holds the extension information for this packet.

## -remarks

Client drivers should not call this function directly. Instead, they should call the appropriate wrapper function for the type of extension they are getting:

- For checksum offload information, the client driver calls [**NetExtensionGetPacketChecksum**](../checksum/nf-checksum-netextensiongetpacketchecksum.md).
- For Generic Segmentation Offload (GSO) information, the client driver calls [**NetExtensionGetPacketLso**](../gso/nf-gso-netextensiongetpacketgso.md).
- For Receive Segment Coalescence (RSC) offload information, the client driver calls [**NetExtensionGetPacketRsc**](../rsc/nf-rsc-netextensiongetpacketrsc.md).

## -see-aextension

[Packet descriptors and extensions](/windows-hardware/drivers/netcx/packet-descriptors-and-extensions)

[Transmit and receive queues](/windows-hardware/drivers/netcx/transmit-and-receive-queues)

[**NetExtensionGetPacketChecksum**](../checksum/nf-checksum-netextensiongetpacketchecksum.md)

[**NetExtensionGetPacketGso**](../gso/nf-gso-netextensiongetpacketgso.md)

[**NetExtensionGetPacketRsc**](../rsc/nf-rsc-netextensiongetpacketrsc.md)
