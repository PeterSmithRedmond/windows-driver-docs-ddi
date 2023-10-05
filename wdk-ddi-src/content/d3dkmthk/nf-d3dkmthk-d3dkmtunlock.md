---
UID: NF:d3dkmthk.D3DKMTUnlock
title: D3DKMTUnlock function (d3dkmthk.h)
description: The D3DKMTUnlock function unlocks a list of allocations.
old-location: display\d3dkmtunlock.htm
ms.date: 03/02/2022
keywords: ["D3DKMTUnlock function"]
ms.keywords: D3DKMTUnlock, D3DKMTUnlock function [Display Devices], OpenGL_Functions_6741960d-1f19-4000-948c-aeb71330eb1e.xml, d3dkmthk/D3DKMTUnlock, display.d3dkmtunlock
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
 - D3DKMTUnlock
 - d3dkmthk/D3DKMTUnlock
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
 - D3DKMTUnlock
---

# D3DKMTUnlock function

## -description

The **D3DKMTUnlock** function unlocks a list of allocations.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_UNLOCK](ns-d3dkmthk-_d3dkmt_unlock.md) structure that describes a list of allocations to unlock.

## -returns

**D3DKMTUnlock** returns one of the following values;

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The allocations were successfully unlocked. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |

This function might also return other **NTSTATUS** values.

## -remarks

All of the allocations that the **D3DKMTUnlock** function unlocks must belong to the same device.

### Examples

The following code examples demonstrates how an OpenGL ICD can use **D3DKMTUnlock** to unlock three allocations.

```cpp
HRESULT UnlockThree(D3DKMT_HANDLE hDevice, 
                    D3DKMT_HANDLE hAllocation1, 
                    D3DKMT_HANDLE hAllocation2, 
                    D3DKMT_HANDLE hAllocation3) 
{
    D3DKMT_HANDLE AllocationArray[3];
    D3DKMT_UNLOCK UnlockData;

    AllocationArray[0] = hAllocation1;
    AllocationArray[1] = hAllocation2;
    AllocationArray[2] = hAllocation3;

    UnlockData.hDevice = hDevice;
    UnlockData.NumAllocations = 3;
    UnlockData.phAllocations = AllocationArray;

    if (NT_SUCCESS((*pfnKTUnlock)(&UnlockData))) {
        return S_OK;
    }
    return E_FAIL;
}
```

## -see-also

[D3DKMT_UNLOCK](ns-d3dkmthk-_d3dkmt_unlock.md)