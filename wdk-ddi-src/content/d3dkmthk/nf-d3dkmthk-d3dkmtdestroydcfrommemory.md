---
UID: NF:d3dkmthk.D3DKMTDestroyDCFromMemory
title: D3DKMTDestroyDCFromMemory function (d3dkmthk.h)
description: The D3DKMTDestroyDCFromMemory function releases the display context.
old-location: display\d3dkmtdestroydcfrommemory.htm
ms.date: 02/23/2022
keywords: ["D3DKMTDestroyDCFromMemory function"]
ms.keywords: D3DKMTDestroyDCFromMemory, D3DKMTDestroyDCFromMemory function [Display Devices], OpenGL_Functions_2c70707b-7052-4f5f-8715-e2e61a7ab267.xml, d3dkmthk/D3DKMTDestroyDCFromMemory, display.d3dkmtdestroydcfrommemory
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
 - D3DKMTDestroyDCFromMemory
 - d3dkmthk/D3DKMTDestroyDCFromMemory
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
 - D3DKMTDestroyDCFromMemory
---

# D3DKMTDestroyDCFromMemory function

## -description

The **D3DKMTDestroyDCFromMemory** function releases the display context.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_DESTROYDCFROMMEMORY](ns-d3dkmthk-_d3dkmt_destroydcfrommemory.md) structure that contains handles to the display context and bitmap.

## -returns

**D3DKMTDestroyDCFromMemory** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The device context was successfully released. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |

This function might also return other **NTSTATUS** values.

## -see-also

[D3DKMT_DESTROYDCFROMMEMORY](ns-d3dkmthk-_d3dkmt_destroydcfrommemory.md)
