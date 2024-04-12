---
UID: NS:d3dkmthk._D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
title: D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS (d3dkmthk.h)
description: Learn more about the D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS structure.
ms.date: 04/10/2024
keywords: ["D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS structure"]
ms.keywords: _D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS, D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS,
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
req.typenames: D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
targetos: Windows
ms.custom: RS5
tech.root: display
f1_keywords:
 - _D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
 - d3dkmthk/_D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
 - D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
 - d3dkmthk/D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3dkmthk.h
api_name:
 - _D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
 - D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS
dev_langs:
 - c++
---

# D3DKMT_PRESENT_MULTIPLANE_OVERLAY_FLAGS structure

## -description

Present multi-plane overlay flags.

## -struct-fields

### -field FlipStereo

Specifies whether the driver should flip both left and right images of a stereo allocation.

### -field FlipStereoTemporaryMono

Specifies whether the driver should use the left image of a stereo allocation for the right and left portions of a stereo frame. The driver performs the same present operation as with **FlipStereo**, except that it should scan out only from the left image to produce both images of a stereo frame.

### -field FlipStereoPreferRight

Specifies that when the driver clones a stereo primary allocation to a mono monitor, it should use the right image.

The **FlipStereoTemporaryMono** and **FlipStereoPreferRight** members can't both be set at the same time.

### -field FlipDoNotWait

A UINT value that specifies whether the OpenGL installable client driver (ICD) requires that the present operation wait for the number of queued flip surfaces to fall below a particular limit before the operation begins. Setting this member indicates that the ICD does not require waiting. The default limit for the number of queued flip surfaces is three.

### -field FlipDoNotFlip

A UINT value that specifies whether to insert queued waits into the rendering stream. Setting this member indicates to flip to the same surface that is currently being scanned out.

### -field FlipRestart

A UINT value that specifies whether to restart a flip to a new surface.

### -field DurationValid

Indicates whether the duration is valid.

### -field HDRMetaDataValid

Indicates whether the HDR metadata is valid.

### -field HMD

The HMD (head mounted display).

### -field TrueImmediate

If a present interval is 0, allow tearing rather than override a previously queued flip.

### -field FromDDisplay

Indicates the present is from DirectDisplay.

### -field Reserved

Reserved for internal use.

### -field Value

The value used to operate over the other members.

## -remarks

## -see-also
