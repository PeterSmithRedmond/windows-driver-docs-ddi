---
UID: NF:d3dkmthk.D3DKMTSetDisplayPrivateDriverFormat
title: D3DKMTSetDisplayPrivateDriverFormat function (d3dkmthk.h)
description: The D3DKMTSetDisplayPrivateDriverFormat function changes the private-format attribute of a video present source.
old-location: display\d3dkmtsetdisplayprivatedriverformat.htm
ms.date: 03/01/2022
keywords: ["D3DKMTSetDisplayPrivateDriverFormat function"]
ms.keywords: D3DKMTSetDisplayPrivateDriverFormat, D3DKMTSetDisplayPrivateDriverFormat function [Display Devices], OpenGL_Functions_742fb584-0b9d-4650-a0a6-64f3e3f55dff.xml, d3dkmthk/D3DKMTSetDisplayPrivateDriverFormat, display.d3dkmtsetdisplayprivatedriverformat
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
 - D3DKMTSetDisplayPrivateDriverFormat
 - d3dkmthk/D3DKMTSetDisplayPrivateDriverFormat
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
 - D3DKMTSetDisplayPrivateDriverFormat
---

# D3DKMTSetDisplayPrivateDriverFormat function

## -description

The **D3DKMTSetDisplayPrivateDriverFormat** function changes the private-format attribute of a video present source.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_SETDISPLAYPRIVATEDRIVERFORMAT](ns-d3dkmthk-_d3dkmt_setdisplayprivatedriverformat.md) structure that describes how to format a video present source.

## -returns

**D3DKMTSetDisplayPrivateDriverFormat** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The video present source was successfully changed. |
| STATUS_DEVICE_REMOVED | The graphics adapter was stopped or the display device was reset. |
|  | Parameters were validated and determined to be incorrect. |
|  | Before the call to **D3DKMTSetDisplayPrivateDriverFormat**, the device did not acquire exclusive ownership of the view. Therefore, the device could not change the private-format attribute of the video present source. |
| STATUS_NOT_SUPPORTED | The display miniport driver does not support the [DXGKDDI_SETDISPLAYPRIVATEDRIVERFORMAT](../d3dkmddi/nc-d3dkmddi-dxgkddi_setdisplayprivatedriverformat.md) function. |
| STATUS_UNSUCCESSFUL | The display miniport driver could not change the private-format attribute of the view for the video present source. |

This function might also return other **NTSTATUS** values.

## -see-also

[D3DKMT_SETDISPLAYPRIVATEDRIVERFORMAT](ns-d3dkmthk-_d3dkmt_setdisplayprivatedriverformat.md)

[DXGKDDI_SETDISPLAYPRIVATEDRIVERFORMAT](../d3dkmddi/nc-d3dkmddi-dxgkddi_setdisplayprivatedriverformat.md)
