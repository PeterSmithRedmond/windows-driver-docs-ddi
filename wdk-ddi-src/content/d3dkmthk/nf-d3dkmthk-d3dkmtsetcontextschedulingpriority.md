---
UID: NF:d3dkmthk.D3DKMTSetContextSchedulingPriority
title: D3DKMTSetContextSchedulingPriority function (d3dkmthk.h)
description: The D3DKMTSetContextSchedulingPriority function sets the scheduling priority for a device context.
old-location: display\d3dkmtsetcontextschedulingpriority.htm
ms.date: 03/01/2022
keywords: ["D3DKMTSetContextSchedulingPriority function"]
ms.keywords: D3DKMTSetContextSchedulingPriority, D3DKMTSetContextSchedulingPriority function [Display Devices], OpenGL_Functions_f9314ed6-8aad-4c55-b42a-f1223dada5bc.xml, d3dkmthk/D3DKMTSetContextSchedulingPriority, display.d3dkmtsetcontextschedulingpriority
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
 - D3DKMTSetContextSchedulingPriority
 - d3dkmthk/D3DKMTSetContextSchedulingPriority
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
 - D3DKMTSetContextSchedulingPriority
---

# D3DKMTSetContextSchedulingPriority function

## -description

The **D3DKMTSetContextSchedulingPriority** function sets the scheduling priority for a device context.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_SETCONTEXTSCHEDULINGPRIORITY](ns-d3dkmthk-_d3dkmt_setcontextschedulingpriority.md) structure that describes parameters for setting the scheduling priority for a device context.

## -returns

**D3DKMTSetContextSchedulingPriority** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The scheduling priority was successfully set. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |

This function might also return other **NTSTATUS** values.

## -see-also

[D3DKMT_SETCONTEXTSCHEDULINGPRIORITY](ns-d3dkmthk-_d3dkmt_setcontextschedulingpriority.md)
