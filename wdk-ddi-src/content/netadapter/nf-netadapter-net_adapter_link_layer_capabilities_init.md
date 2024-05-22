---
UID: NF:netadapter.NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT
title: NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT function (netadapter.h)
description: Initializes the NET_ADAPTER_LINK_LAYER_CAPABILITIES structure.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT function"]
ms.keywords: NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 1.23
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
req.alt-api: 
req.alt-loc: 
req.typenames: NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT
targetos: Windows
f1_keywords:
 - NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT
 - netadapter/NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT
---

# NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT function


## -description

The **NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT** function initializes a [NET_ADAPTER_LINK_LAYER_CAPABILITIES](ns-netadapter-_net_adapter_link_layer_capabilities.md) structure.

## -parameters

### -param LinkLayerCapabilities [_Out_]

A pointer to the driver-allocated [NET_ADAPTER_LINK_LAYER_CAPABILITIES](ns-netadapter-_net_adapter_link_layer_capabilities.md) structure that describes the link layer capabilities of the adapter.

### -param MaxTxLinkSpeed [_In_]

The maximum transmit link speed of the adapter in bits per second. For more information, see [OID_GEN_MAX_LINK_SPEED](/windows-hardware/drivers/network/oid-gen-max-link-speed).

### -param MaxRxLinkSpeed [_In_]

The maximum receive link speed of the adapter in bits per second. For more information, see [OID_GEN_MAX_LINK_SPEED](/windows-hardware/drivers/network/oid-gen-max-link-speed).

## -remarks

**NET_ADAPTER_LINK_LAYER_CAPABILITIES_INIT** zeroes out the [NET_ADAPTER_LINK_LAYER_CAPABILITIES](ns-netadapter-_net_adapter_link_layer_capabilities.md) structure and then sets all of its members.

## -see-also
