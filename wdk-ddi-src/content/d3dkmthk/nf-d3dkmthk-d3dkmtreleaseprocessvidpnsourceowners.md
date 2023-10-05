---
UID: NF:d3dkmthk.D3DKMTReleaseProcessVidPnSourceOwners
title: D3DKMTReleaseProcessVidPnSourceOwners function (d3dkmthk.h)
description: The D3DKMTReleaseProcessVidPnSourceOwners function releases the video present network source owners for a process.
old-location: display\d3dkmtreleaseprocessvidpnsourceowners.htm
ms.date: 05/10/2018
keywords: ["D3DKMTReleaseProcessVidPnSourceOwners function"]
ms.keywords: D3DKMTReleaseProcessVidPnSourceOwners, D3DKMTReleaseProcessVidPnSourceOwners function [Display Devices], OpenGL_Functions_8c1e2870-c803-4ca4-99f1-8f39a00983c8.xml, d3dkmthk/D3DKMTReleaseProcessVidPnSourceOwners, display.d3dkmtreleaseprocessvidpnsourceowners
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
 - D3DKMTReleaseProcessVidPnSourceOwners
 - d3dkmthk/D3DKMTReleaseProcessVidPnSourceOwners
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
 - D3DKMTReleaseProcessVidPnSourceOwners
---

# D3DKMTReleaseProcessVidPnSourceOwners function


## -description

The <b>D3DKMTReleaseProcessVidPnSourceOwners</b> function releases the video present network source owners for a process.

## -parameters

### -param unnamedParam1 [in]

*hProcess* 

A handle to the process that video present network source owners are released from.

## -returns

<b>D3DKMTReleaseProcessVidPnSourceOwners</b> returns one of the following values:

|Return code|Description|
|--- |--- |
|STATUS_SUCCESS|The video present network source owners for a process were successfully released.|
|STATUS_INVALID_PARAMETER|Parameters were validated and determined to be incorrect.|

This function might also return other <b>NTSTATUS</b> values.

