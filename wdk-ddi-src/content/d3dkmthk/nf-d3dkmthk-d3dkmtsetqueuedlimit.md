---
UID: NF:d3dkmthk.D3DKMTSetQueuedLimit
title: D3DKMTSetQueuedLimit function (d3dkmthk.h)
description: The D3DKMTSetQueuedLimit function sets or retrieves the limit for the number of operations of the given type that can be queued for the given device.
old-location: display\d3dkmtsetqueuedlimit.htm
ms.date: 03/01/2022
keywords: ["D3DKMTSetQueuedLimit function"]
ms.keywords: D3DKMTSetQueuedLimit, D3DKMTSetQueuedLimit function [Display Devices], OpenGL_Functions_22227369-eb8b-4ee0-a3d8-97eb0f469d94.xml, d3dkmthk/D3DKMTSetQueuedLimit, display.d3dkmtsetqueuedlimit
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
 - D3DKMTSetQueuedLimit
 - d3dkmthk/D3DKMTSetQueuedLimit
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
 - D3DKMTSetQueuedLimit
---

# D3DKMTSetQueuedLimit function

## -description

The **D3DKMTSetQueuedLimit** function sets or retrieves the limit for the number of operations of the given type that can be queued for the given device.

## -parameters

### -param unnamedParam1 [in]

A pointer to a [D3DKMT_SETQUEUEDLIMIT](ns-d3dkmthk-_d3dkmt_setqueuedlimit.md) structure that describes parameters for setting or retrieving the limit of queued operations.

## -returns

**D3DKMTSetQueuedLimit** returns one of the following values:

| Return code | Description |
|--|--|
| STATUS_SUCCESS | The limit of queued operations was successfully set or retrieved. |
| STATUS_DEVICE_REMOVED | The graphics adapter was stopped or the display device was reset. |
| STATUS_INVALID_PARAMETER | Parameters were validated and determined to be incorrect. |

This function might also return other **NTSTATUS** values.

## -see-also

[D3DKMT_QUEUEDLIMIT_TYPE](ne-d3dkmthk-_d3dkmt_queuedlimit_type.md)

[D3DKMT_SETQUEUEDLIMIT](ns-d3dkmthk-_d3dkmt_setqueuedlimit.md)