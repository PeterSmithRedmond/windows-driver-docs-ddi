---
UID: NE:netadapter._NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
title: _NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE (netadapter.h)
description: The NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE enumeration identifies how the operating system should allocate NET_PACKET_FRAGMENT receive buffers for a net adapter client driver's receive queues.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE enumeration"]
ms.keywords: _NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE, NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE,
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.25
req.umdf-ver: 2.33 
req.ddi-compliance: 
req.max-support: 
req.typenames: NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
targetos: Windows
f1_keywords:
 - _NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
 - netadapter/_NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
 - NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
 - netadapter/NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - _NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
 - NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE
---

# _NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE enumeration


## -description

The **NET_RX_FRAGMENT_BUFFER_ALLOCATION_MODE** enumeration identifies how the operating system should allocate [NET_FRAGMENT](../fragment/ns-fragment-_net_fragment.md) receive buffers for a net adapter client driver's receive queues.

## -enum-fields

### -field NetRxFragmentBufferAllocationModeSystem:0 

The operating system allocates [NET_FRAGMENT](../fragment/ns-fragment-_net_fragment.md) receive buffers on behalf of the client driver.

### -field NetRxFragmentBufferAllocationModeDriver:1 

The operating system never allocates [NET_FRAGMENT](../fragment/ns-fragment-_net_fragment.md) receive buffers. The client driver is responsible for buffer allocation.

## -remarks

This enumeration is a value of the [NET_ADAPTER_RX_CAPABILITIES](ns-netadapter-_net_adapter_rx_capabilities.md) structure. Together with [NET_RX_FRAGMENT_BUFFER_ATTACHMENT_MODE](ne-netadapter-_net_rx_fragment_buffer_attachment_mode.md), it specifies how a net adapter client driver would like to configure its receive queue fragment buffers. For more information, see [NET_ADAPTER_RX_CAPABILITIES](ns-netadapter-_net_adapter_rx_capabilities.md).

## -see-also

[NET_ADAPTER_RX_CAPABILITIES](ns-netadapter-_net_adapter_rx_capabilities.md)

