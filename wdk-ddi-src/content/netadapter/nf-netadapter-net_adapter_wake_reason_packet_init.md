---
UID: NF:netadapter.NET_ADAPTER_WAKE_REASON_PACKET_INIT
title: NET_ADAPTER_WAKE_REASON_PACKET_INIT function (netadapter.h)
description: The NET_ADAPTER_WAKE_REASON_PACKET_INIT function initializes a NET_ADAPTER_WAKE_REASON_PACKET structure.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_ADAPTER_WAKE_REASON_PACKET_INIT function"]
ms.keywords: NET_ADAPTER_WAKE_REASON_PACKET_INIT
req.header: netadaptercx.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
ms.custom: Vb
f1_keywords:
 - NET_ADAPTER_WAKE_REASON_PACKET_INIT
 - netadapter/NET_ADAPTER_WAKE_REASON_PACKET_INIT
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - NET_ADAPTER_WAKE_REASON_PACKET_INIT
---

# NET_ADAPTER_WAKE_REASON_PACKET_INIT function


## -description

The **NET_ADAPTER_WAKE_REASON_PACKET_INIT** function initializes a [**NET_ADAPTER_WAKE_REASON_PACKET**](../netadapter/ns-netadapter-_net_adapter_wake_reason_packet.md) structure.

## -parameters

### -param Reason [_Out_]

A pointer to a driver allocated [**NET_ADAPTER_WAKE_REASON_PACKET**](../netadapter/ns-netadapter-_net_adapter_wake_reason_packet.md) structure.


## -remarks

This function zeroes out the memory for the **NET_ADAPTER_WAKE_REASON_PACKET** structure, then sets the **Size** member.

## -see-also

[Configuring power management](/windows-hardware/drivers/netcx/configuring-power-management)

[**NET_ADAPTER_WAKE_REASON_PACKET**](../netadapter/ns-netadapter-_net_adapter_wake_reason_packet.md)
