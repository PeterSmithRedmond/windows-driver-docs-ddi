---
UID: NF:nettxqueue.NetTxQueueGetExtension
title: NetTxQueueGetExtension function (nettxqueue.h)
description: The NetTxQueueGetExtension function retrieves a packet extension for all packets in a transmit (Tx) queue.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NetTxQueueGetExtension function"]
ms.keywords: NetTxQueueGetExtension
req.header: nettxqueue.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.29
req.umdf-ver: 2.33 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - NetTxQueueGetExtension
 - nettxqueue/NetTxQueueGetExtension
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - NetTxQueueGetExtension
---

# NetTxQueueGetExtension function


## -description

The **NetTxQueueGetExtension** function retrieves a packet extension for all packets in a transmit (Tx) queue.

## -parameters

### -param PacketQueue [_In_]

The transmit queue object.

### -param Query [_In_]

A pointer to a driver-allocated and initialized [**NET_EXTENSION_QUERY**](../netadapterpacket/ns-netadapterpacket-_net_extension_query.md) structure that contains information about the desired packet extension.

### -param Extension [_Out_]

A handle to a driver-allocated [**NET_EXTENSION**](../extension/ns-extension-_net_extension.md) structure that receives the packet extension.

## -remarks

Client drivers typically call this function from their *[EvtNetAdapterCreateTxQueue](../netadapter/nc-netadapter-evt_net_adapter_create_txqueue.md)* callback function after queue creation. To prevent frequent extension queries, store the extension returned by this function in your queue context space.

For a code example of creating a transmit queue, see [Transmit and receive queues](/windows-hardware/drivers/netcx/transmit-and-receive-queues).

## -see-also

[Packet descriptors and extensions](/windows-hardware/drivers/netcx/packet-descriptors-and-extensions)
