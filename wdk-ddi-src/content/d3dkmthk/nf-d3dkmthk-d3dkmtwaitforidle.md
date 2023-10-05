---
UID: NF:d3dkmthk.D3DKMTWaitForIdle
title: D3DKMTWaitForIdle function (d3dkmthk.h)
description: The D3DKMTWaitForIdle function waits for a display device to be idle.
old-location: display\d3dkmtwaitforidle.htm
ms.date: 05/10/2018
keywords: ["D3DKMTWaitForIdle function"]
ms.keywords: D3DKMTWaitForIdle, D3DKMTWaitForIdle function [Display Devices], OpenGL_Functions_80855290-d991-4e03-aa64-f0fb486c57b0.xml, d3dkmthk/D3DKMTWaitForIdle, display.d3dkmtwaitforidle
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
 - D3DKMTWaitForIdle
 - d3dkmthk/D3DKMTWaitForIdle
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
 - D3DKMTWaitForIdle
---

# D3DKMTWaitForIdle function


## -description

The <b>D3DKMTWaitForIdle</b> function waits for a display device to be idle.

## -parameters

### -param D3DKMT_WAITFORIDLE

*pData* [in]

A pointer to a <a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_waitforidle">D3DKMT_WAITFORIDLE</a> structure that specifies the display device to wait for.

## -returns

<b>D3DKMTWaitForIdle</b> returns one of the following values:

|Return code|Description|
|--- |--- |
|STATUS_SUCCESS|The wait for the display device successfully occurred.|
|STATUS_INVALID_PARAMETER|Parameters were validated and determined to be incorrect.|

This function might also return other NTSTATUS values.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_waitforidle">D3DKMT_WAITFORIDLE</a>
