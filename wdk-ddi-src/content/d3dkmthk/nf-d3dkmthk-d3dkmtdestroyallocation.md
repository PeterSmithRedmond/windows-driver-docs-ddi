---
UID: NF:d3dkmthk.D3DKMTDestroyAllocation
title: D3DKMTDestroyAllocation function (d3dkmthk.h)
description: The D3DKMTDestroyAllocation function releases a resource, a list of allocations, or both.
old-location: display\d3dkmtdestroyallocation.htm
ms.date: 02/23/2022
keywords: ["D3DKMTDestroyAllocation function"]
ms.keywords: D3DKMTDestroyAllocation, D3DKMTDestroyAllocation function [Display Devices], OpenGL_Functions_ecc5579c-3b0a-4c2c-9978-9f2591444c03.xml, d3dkmthk/D3DKMTDestroyAllocation, display.d3dkmtdestroyallocation
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
 - D3DKMTDestroyAllocation
 - d3dkmthk/D3DKMTDestroyAllocation
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
 - D3DKMTDestroyAllocation
---

# D3DKMTDestroyAllocation function

## -description

The **D3DKMTDestroyAllocation** function releases a resource, a list of allocations, or both.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_DESTROYALLOCATION](ns-d3dkmthk-_d3dkmt_destroyallocation.md) structure that contains information for releasing allocations.

## -returns

**D3DKMTDestroyAllocation** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | Allocations were successfully released. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |

This function might also return other **NTSTATUS** values.

## -see-also

[D3DKMT_DESTROYALLOCATION](ns-d3dkmthk-_d3dkmt_destroyallocation.md)
