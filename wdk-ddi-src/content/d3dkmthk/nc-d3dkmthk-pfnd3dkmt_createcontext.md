---
UID: NC:d3dkmthk.PFND3DKMT_CREATECONTEXT
title: PFND3DKMT_CREATECONTEXT (d3dkmthk.h)
description: The PFND3DKMT_CREATECONTEXT callback creates a kernel-mode device context. The function returns STATUS_SUCCESS on successful creation of the device context.
old-location: display\d3dkmtcreatecontext.htm
ms.date: 05/10/2018
keywords: ["PFND3DKMT_CREATECONTEXT callback function"]
ms.keywords: D3DKMTCreateContext, D3DKMTCreateContext callback function [Display Devices], OpenGL_Functions_ee92f6d8-b9af-4171-a628-e686f190a370.xml, PFND3DKMT_CREATECONTEXT, PFND3DKMT_CREATECONTEXT callback, d3dkmthk/D3DKMTCreateContext, display.d3dkmtcreatecontext
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
tech.root: display
req.typenames: 
f1_keywords:
 - PFND3DKMT_CREATECONTEXT
 - d3dkmthk/PFND3DKMT_CREATECONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - d3dkmthk.h
api_name:
 - PFND3DKMT_CREATECONTEXT
---

# PFND3DKMT_CREATECONTEXT callback function


## -description

The <b>D3DKMTCreateContext</b> function creates a kernel-mode device context.

## -parameters

### -param unnamedParam1

*pData* [in, out]

A pointer to a <a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_createcontext">D3DKMT_CREATECONTEXT</a> structure that describes the kernel-mode device context.

## -returns

<b>D3DKMTCreateContext</b> returns one of the following values:

| **Return code** | **Description** |
|:--|:--|
| **STATUS_SUCCESS** | The device context was successfully created. |
| **STATUS_DEVICE_REMOVED** | The graphics adapter was stopped or the display device was reset. |
| **STATUS_INVALID_PARAMETER** | Parameters were validated and determined to be incorrect. |
| **STATUS_NO_MEMORY** | [D3DKMTCreateContext](./nf-d3dkmthk-d3dkmtcreatecontext.md)  could not complete because of insufficient memory. |

This function might also return other <b>NTSTATUS</b> values.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_createcontext">D3DKMT_CREATECONTEXT</a>

