---
UID: NF:d3dkmthk.D3DKMTFlipOverlay
title: D3DKMTFlipOverlay function (d3dkmthk.h)
description: The D3DKMTFlipOverlay function changes the allocation to display on the overlay.
old-location: display\d3dkmtflipoverlay.htm
ms.date: 02/25/2022
keywords: ["D3DKMTFlipOverlay function"]
ms.keywords: D3DKMTFlipOverlay, D3DKMTFlipOverlay function [Display Devices], OpenGL_Functions_37a9811c-26a3-46f3-aba1-39dc9526f282.xml, d3dkmthk/D3DKMTFlipOverlay, display.d3dkmtflipoverlay
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Universal
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
tech.root: display
req.typenames: 
f1_keywords:
 - D3DKMTFlipOverlay
 - d3dkmthk/D3DKMTFlipOverlay
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - API-MS-Win-dx-d3dkmt-l1-1-0.dll
 - API-MS-Win-dx-d3dkmt-l1-1-1.dll
 - API-MS-Win-DX-D3DKMT-L1-1-2.dll
api_name:
 - D3DKMTFlipOverlay
---

# D3DKMTFlipOverlay function

## -description

The **D3DKMTFlipOverlay** function changes the allocation to display on the overlay.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_FLIPOVERLAY](ns-d3dkmthk-_d3dkmt_flipoverlay.md) structure that describes how to change the display on the overlay.

## -returns

**D3DKMTFlipOverlay** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The kernel-mode overlay object was successfully flipped. |
| STATUS_DEVICE_REMOVED | The graphics adapter was stopped or the display device was reset. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |
| STATUS_NO_MEMORY | **D3DKMTFlipOverlay** could not complete because of insufficient memory. |

This function might also return other **NTSTATUS** values.

## -see-also

[D3DKMT_FLIPOVERLAY](ns-d3dkmthk-_d3dkmt_flipoverlay.md)