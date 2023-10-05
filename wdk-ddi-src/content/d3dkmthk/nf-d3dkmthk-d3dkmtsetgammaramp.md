---
UID: NF:d3dkmthk.D3DKMTSetGammaRamp
title: D3DKMTSetGammaRamp function (d3dkmthk.h)
description: The D3DKMTSetGammaRamp function sets the gamma ramp.
old-location: display\d3dkmtsetgammaramp.htm
ms.date: 03/01/2022
keywords: ["D3DKMTSetGammaRamp function"]
ms.keywords: D3DKMTSetGammaRamp, D3DKMTSetGammaRamp function [Display Devices], OpenGL_Functions_4d684cea-8528-489d-bc35-b70a5f05a57b.xml, d3dkmthk/D3DKMTSetGammaRamp, display.d3dkmtsetgammaramp
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
 - D3DKMTSetGammaRamp
 - d3dkmthk/D3DKMTSetGammaRamp
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
 - D3DKMTSetGammaRamp
---

# D3DKMTSetGammaRamp function

## -description

The **D3DKMTSetGammaRamp** function sets the gamma ramp.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_SETGAMMARAMP](ns-d3dkmthk-_d3dkmt_setgammaramp.md) structure that describes parameters for setting the gamma ramp.

## -returns

**D3DKMTSetGammaRamp** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The gamma ramp was successfully set. |
| STATUS_DEVICE_REMOVED | The graphics adapter was stopped. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |

This function might also return other **NTSTATUS** values.

## -see-also

[D3DKMT_SETGAMMARAMP](ns-d3dkmthk-_d3dkmt_setgammaramp.md)