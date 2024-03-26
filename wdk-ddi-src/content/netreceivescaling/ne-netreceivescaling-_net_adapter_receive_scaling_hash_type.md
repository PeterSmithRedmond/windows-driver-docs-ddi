---
UID: NE:netreceivescaling._NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
title: _NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE (netreceivescaling.h)
description: The NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE enumeration specifies the type of receive side scaling (RSS) hash function that a NIC should use to compute the hash values for incoming packets.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE enumeration"]
ms.keywords: _NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE, NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE,
req.header: netreceivescaling.h
req.include-header: netadaptercx.h
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.25
req.umdf-ver: 2.33 
req.ddi-compliance: 
req.max-support: 
req.typenames: NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
targetos: Windows
f1_keywords:
 - _NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
 - netreceivescaling/_NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
 - NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
 - netreceivescaling/NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netreceivescaling.h
api_name:
 - _NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
 - NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE
---

# _NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE enumeration


## -description

The **NET_ADAPTER_RECEIVE_SCALING_HASH_TYPE** enumeration specifies the type of receive side scaling (RSS) hash function that a NIC should use to compute the hash values for incoming packets.

## -enum-fields

### -field NetAdapterReceiveScalingHashTypeNone:0x00000000 

Unused for RSS-capable NIC client drivers.

### -field NetAdapterReceiveScalingHashTypeToeplitz:0x00000001 

Indicates support for the Toeplitz hashing function.

## -remarks

Currently, **NetAdapterReceiveScalingHashTypeToeplitz** is the only hashing function available to NIC client drivers.

## -see-also

[NetAdapterCx Receive Side Scaling](/windows-hardware/drivers/netcx/netadaptercx-receive-side-scaling-rss-)

