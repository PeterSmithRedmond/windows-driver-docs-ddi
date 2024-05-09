---
UID: NS:d3dkmthk._D3DKMT_MULTIPLANE_OVERLAY3
title: D3DKMT_MULTIPLANE_OVERLAY3 (d3dkmthk.h)
description: Learn more about the D3DKMT_MULTIPLANE_OVERLAY3 structure.
ms.date: 04/10/2024
keywords: ["D3DKMT_MULTIPLANE_OVERLAY3 structure"]
ms.keywords: _D3DKMT_MULTIPLANE_OVERLAY3, D3DKMT_MULTIPLANE_OVERLAY3,
req.header: d3dkmthk.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3DKMT_MULTIPLANE_OVERLAY3
targetos: Windows
ms.custom: RS5
tech.root: display
f1_keywords:
 - _D3DKMT_MULTIPLANE_OVERLAY3
 - d3dkmthk/_D3DKMT_MULTIPLANE_OVERLAY3
 - D3DKMT_MULTIPLANE_OVERLAY3
 - d3dkmthk/D3DKMT_MULTIPLANE_OVERLAY3
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3dkmthk.h
api_name:
 - _D3DKMT_MULTIPLANE_OVERLAY3
 - D3DKMT_MULTIPLANE_OVERLAY3
dev_langs:
 - c++
---

# D3DKMT_MULTIPLANE_OVERLAY3 structure

## -description

Multiplane overlay structure.

## -struct-fields

### -field LayerIndex

The layer index.

### -field InputFlags

The input flags.

### -field FlipInterval

A UINT value that specifies whether the display miniport driver natively supports the scheduling of a flip command to take effect after two, three or four vertical syncs occur.

### -field MaxImmediateFlipLine

The maximum immediate flip line.

### -field AllocationCount

Number of allocations in *pAllocationList*.

### -field pAllocationList

Pointer to the first allocation list.

### -field DriverPrivateDataSize

The driver private data size.

### -field pDriverPrivateData

Pointer to driver private data.

### -field pPlaneAttributes

A structure that contains the plane attributes.

### -field hFlipToFence

Handle to the fence for a flip that is about to occur.

### -field hFlipAwayFence

Handle to the fence for a flip that has just completed.

### -field FlipToFenceValue

Fence value for the flip that is about to occur.

## -field FlipAwayFenceValue

Fence value for the flip that has just completed.

## -see-also

[**D3DKMT_PRESENT_MULTIPLANE_OVERLAY3**](ns-d3dkmthk-_d3dkmt_present_multiplane_overlay3.md)
