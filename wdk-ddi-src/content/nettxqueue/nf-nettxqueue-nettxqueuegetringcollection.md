---
UID: NF:nettxqueue.NetTxQueueGetRingCollection
title: NetTxQueueGetRingCollection function (nettxqueue.h)
description: The NetTxQueueGetRingCollection function retrieves the NET_DATAPATH_DESCRIPTOR structure for a transmit (Tx) queue.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NetTxQueueGetRingCollection function"]
ms.keywords: NetTxQueueGetRingCollection
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
 - NetTxQueueGetRingCollection
 - nettxqueue/NetTxQueueGetRingCollection
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - NetTxQueueGetRingCollection
---

# NetTxQueueGetRingCollection function


## -description

The **NetTxQueueGetRingCollection** function retrieves the [**NET_RING_COLLECTION**](../ringcollection/ns-ringcollection-_net_ring_collection.md) structure for a transmit (Tx) queue.

## -parameters

### -param PacketQueue [_In_]

A pointer to a NetAdapterCx-allocated **NETPACKETQUEUE** structure. The client driver receives a pointer to this **NETPACKETQUEUE** structure in its *[EVT_NET_ADAPTER_CREATE_TXQUEUE](../netadapter/nc-netadapter-evt_net_adapter_create_txqueue.md)* callback function.

## -returns

Returns a pointer to the queue's [**NET_RING_COLLECTION**](../ringcollection/ns-ringcollection-_net_ring_collection.md) structure.

## -remarks

Use the [**NET_RING_COLLECTION**](../ringcollection/ns-ringcollection-_net_ring_collection.md) structure returned by this function to access a transmit queue's net rings.

## -see-also

