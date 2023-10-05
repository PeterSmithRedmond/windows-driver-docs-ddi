---
UID: NF:d3dkmthk.D3DKMTCreateSynchronizationObject
title: D3DKMTCreateSynchronizationObject function (d3dkmthk.h)
description: The D3DKMTCreateSynchronizationObject function creates a kernel-mode synchronization object.
old-location: display\d3dkmtcreatesynchronizationobject.htm
ms.date: 05/10/2018
keywords: ["D3DKMTCreateSynchronizationObject function"]
ms.keywords: D3DKMTCreateSynchronizationObject, D3DKMTCreateSynchronizationObject function [Display Devices], OpenGL_Functions_505065c6-f259-4518-adb8-f7d0fa6b56a5.xml, d3dkmthk/D3DKMTCreateSynchronizationObject, display.d3dkmtcreatesynchronizationobject
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
 - D3DKMTCreateSynchronizationObject
 - d3dkmthk/D3DKMTCreateSynchronizationObject
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
 - D3DKMTCreateSynchronizationObject
---

# D3DKMTCreateSynchronizationObject function


## -description

The <b>D3DKMTCreateSynchronizationObject</b> function creates a kernel-mode synchronization object.

## -parameters

### -param unnamedParam1

*pData* [in, out]

A pointer to a <a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_createsynchronizationobject">D3DKMT_CREATESYNCHRONIZATIONOBJECT</a> structure that describes a synchronization object.

## -returns

<b>D3DKMTCreateSynchronizationObject</b> returns one of the following values:

| **Return code** | **Description** | 
|:--|:--|
| **STATUS_SUCCESS** | The kernel-mode synchronization object was successfully created. | 
| **STATUS_DEVICE_REMOVED** | The graphics adapter was stopped or the display device was reset. | 
| **STATUS_INVALID_PARAMETER** | Parameters were validated and determined to be incorrect. | 
| **STATUS_NO_MEMORY** | [D3DKMTCreateSynchronizationObject]() could not complete because of insufficient memory. | 

This function might also return other <b>NTSTATUS</b> values.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_createsynchronizationobject">D3DKMT_CREATESYNCHRONIZATIONOBJECT</a>
