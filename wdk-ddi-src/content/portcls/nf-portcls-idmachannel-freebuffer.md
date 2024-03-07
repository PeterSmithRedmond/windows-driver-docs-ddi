---
UID: NF:portcls.IDmaChannel.FreeBuffer
title: IDmaChannel::FreeBuffer (portcls.h)
description: The FreeBuffer method frees the buffer that was allocated by the previous call to IDmaChannel::AllocateBuffer.
tech.root: audio
ms.date: 10/31/2018
keywords: ["IDmaChannel::FreeBuffer"]
ms.keywords: IDmaChannel::FreeBuffer, FreeBuffer, IDmaChannel.FreeBuffer, IDmaChannel::FreeBuffer, IDmaChannel.FreeBuffer
req.header: portcls.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
 - IDmaChannel::FreeBuffer
 - portcls/IDmaChannel::FreeBuffer
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - portcls.h
api_name:
 - IDmaChannel::FreeBuffer
---

# IDmaChannel::FreeBuffer


## -description

The FreeBuffer method frees the buffer that was allocated by the previous call to IDmaChannel::AllocateBuffer.

## -remarks

Because the buffer is automatically freed when the DMA-channel object is deleted, the FreeBuffer method is not typically used.

## -see-also

[IDmaChannel](nn-portcls-idmachannel.md)

