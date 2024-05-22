---
UID: NE:netadapter._NET_MEMORY_MAPPING_REQUIREMENT
title: _NET_MEMORY_MAPPING_REQUIREMENT (netadapter.h)
description: The NET_MEMORY_MAPPING_REQUIREMENT enumeration identifies the memory mapping requirement that a net adapter can specify for its receive and transmit buffers.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_MEMORY_MAPPING_REQUIREMENT enumeration"]
ms.keywords: _NET_MEMORY_MAPPING_REQUIREMENT, NET_MEMORY_MAPPING_REQUIREMENT, *PNET_MEMORY_MAPPING_REQUIREMENT,
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.25
req.umdf-ver: 2.33 
req.ddi-compliance: 
req.max-support: 
req.typenames: NET_MEMORY_MAPPING_REQUIREMENT, *PNET_MEMORY_MAPPING_REQUIREMENT
targetos: Windows
f1_keywords:
 - _NET_MEMORY_MAPPING_REQUIREMENT
 - netadapter/_NET_MEMORY_MAPPING_REQUIREMENT
 - NET_MEMORY_MAPPING_REQUIREMENT
 - netadapter/NET_MEMORY_MAPPING_REQUIREMENT
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - _NET_MEMORY_MAPPING_REQUIREMENT
 - NET_MEMORY_MAPPING_REQUIREMENT
---

# _NET_MEMORY_MAPPING_REQUIREMENT enumeration


## -description

The **NET_MEMORY_MAPPING_REQUIREMENT** enumeration identifies the memory mapping requirement that a net adapter can specify for its receive and transmit buffers.

## -enum-fields

### -field NetMemoryMappingRequirementNone:0 

The adapter does not require memory mapping.

### -field NetMemoryMappingRequirementDmaMapped:1 

The adapter requires DMA mapping for mapping receive or transmit buffers.

## -remarks

## -see-also

[NET_ADAPTER_RX_CAPABILITIES](ns-netadapter-_net_adapter_rx_capabilities.md)

[NET_ADAPTER_TX_CAPABILITIES](ns-netadapter-_net_adapter_tx_capabilities.md)

