---
UID: NF:netpacketqueue.NET_PACKET_QUEUE_CONFIG_INIT
title: NET_PACKET_QUEUE_CONFIG_INIT function (netpacketqueue.h)
description: The NET_PACKET_QUEUE_CONFIG_INIT function initializes a NET_PACKET_QUEUE_CONFIG structure.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NET_PACKET_QUEUE_CONFIG_INIT function"]
ms.keywords: NET_PACKET_QUEUE_CONFIG_INIT
req.header: netpacketqueue.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.27
req.umdf-ver: 
req.lib: netadaptercxstub.lib
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
ms.custom: RS5
f1_keywords:
 - NET_PACKET_QUEUE_CONFIG_INIT
 - netpacketqueue/NET_PACKET_QUEUE_CONFIG_INIT
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NET_PACKET_QUEUE_CONFIG_INIT
---

# NET_PACKET_QUEUE_CONFIG_INIT function


## -description

The **NET_PACKET_QUEUE_CONFIG_INIT** function initializes a [**NET_PACKET_QUEUE_CONFIG**](ns-netpacketqueue-_net_packet_queue_config.md) structure.

## -parameters

### -param Config [_Out_]

A pointer to the driver-allocated [**NET_PACKET_QUEUE_CONFIG**](ns-netpacketqueue-_net_packet_queue_config.md) structure to initialize.

### -param EvtAdvance [_In_]

A pointer to the client driver's implementation of the [*EVT_PACKET_QUEUE_ADVANCE*](nc-netpacketqueue-evt_packet_queue_advance.md) callback function for this packet queue.

### -param EvtSetNotificationEnabled [_In_]

A pointer to the client driver's implementation of the [*EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED*](nc-netpacketqueue-evt_packet_queue_advance.md) callback function for this packet queue.

### -param EvtCancel [_In_]

A pointer to the client driver's implementation of the [*EVT_PACKET_QUEUE_CANCEL*](nc-netpacketqueue-evt_packet_queue_cancel.md) callback function for this packet queue.

## -remarks

Client drivers must call this function to initialize a [**NET_PACKET_QUEUE_CONFIG**](ns-netpacketqueue-_net_packet_queue_config.md) structure before calling [**NetTxQueueCreate**](../nettxqueue/nf-nettxqueue-nettxqueuecreate.md) or [**NetRxQueueCreate**](../netrxqueue/nf-netrxqueue-netrxqueuecreate.md) to create a packet queue.

## -see-also

[**NET_PACKET_QUEUE_CONFIG**](ns-netpacketqueue-_net_packet_queue_config.md)

[**NetTxQueueCreate**](../nettxqueue/nf-nettxqueue-nettxqueuecreate.md)

[**NetRxQueueCreate**](../netrxqueue/nf-netrxqueue-netrxqueuecreate.md)

