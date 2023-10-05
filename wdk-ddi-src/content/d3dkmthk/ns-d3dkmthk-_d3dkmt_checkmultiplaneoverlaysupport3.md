---
UID: NS:d3dkmthk._D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
title: D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3 (d3dkmthk.h)
description: The _D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3 structure contains information that is used to check for multiplane overlay support.
ms.date: 10/19/2018
keywords: ["D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3 structure"]
ms.keywords: _D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3, D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3,
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
req.typenames: D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
targetos: Windows
ms.custom: RS5
tech.root: display
f1_keywords:
 - _D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
 - d3dkmthk/_D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
 - D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
 - d3dkmthk/D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3dkmthk.h
api_name:
 - _D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
 - D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3
dev_langs:
 - c++
---

# D3DKMT_CHECKMULTIPLANEOVERLAYSUPPORT3 structure

## -description

Check for multiplane overlay support.

## -struct-fields

### -field hAdapter

A handle to the graphics adapter.

### -field hDevice

A handle to the device.

### -field PlaneCount

The number of resources to pin.

### -field pOverlayPlanes

Array of pointers to overlay planes.

### -field PostCompositionCount

The number of resources to pin.

### -field ppPostComposition

Array of pointers to overlay planes.

### -field Supported

Indicates support.

### -field ReturnInfo

The return info.

## -remarks

## -see-also
