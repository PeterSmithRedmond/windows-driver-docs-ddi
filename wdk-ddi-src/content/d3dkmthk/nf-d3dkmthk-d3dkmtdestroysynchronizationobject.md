---
UID: NF:d3dkmthk.D3DKMTDestroySynchronizationObject
title: D3DKMTDestroySynchronizationObject function (d3dkmthk.h)
description: Learn more about the D3DKMTDestroySynchronizationObject function.
ms.date: 04/08/2024
keywords: ["D3DKMTDestroySynchronizationObject function"]
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
 - D3DKMTDestroySynchronizationObject
 - d3dkmthk/D3DKMTDestroySynchronizationObject
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
 - D3DKMTDestroySynchronizationObject
---

## -description

The **D3DKMTDestroySynchronizationObject** function destroys a kernel-mode synchronization object.

## -parameters

### -param unnamedParam1 [in]

Pointer to a [**D3DKMT_DESTROYSYNCHRONIZATIONOBJECT**](ns-d3dkmthk-_d3dkmt_destroysynchronizationobject.md) structure that contains the handle to the synchronization object to destroy.

## -returns

**D3DKMTDestroySynchronizationObject** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The kernel-mode overlay object was successfully destroyed. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |

This function might also return other **NTSTATUS** values.

## -see-also

[**D3DKMT_DESTROYSYNCHRONIZATIONOBJECT**](ns-d3dkmthk-_d3dkmt_destroysynchronizationobject.md)
