---
UID: NS:d3dkmthk._D3DKMT_DESTROYCONTEXT
title: _D3DKMT_DESTROYCONTEXT (d3dkmthk.h)
description: The D3DKMT_DESTROYCONTEXT structure contains a handle to a kernel-mode device context to release.
old-location: display\d3dkmt_destroycontext.htm
ms.date: 05/10/2018
keywords: ["D3DKMT_DESTROYCONTEXT structure"]
ms.keywords: D3DKMT_DESTROYCONTEXT, D3DKMT_DESTROYCONTEXT structure [Display Devices], OpenGL_Structs_97f52665-09e6-4f11-b2cc-a7abcc61827c.xml, _D3DKMT_DESTROYCONTEXT, d3dkmthk/D3DKMT_DESTROYCONTEXT, display.d3dkmt_destroycontext
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Windows
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
req.typenames: D3DKMT_DESTROYCONTEXT
f1_keywords:
 - _D3DKMT_DESTROYCONTEXT
 - d3dkmthk/_D3DKMT_DESTROYCONTEXT
 - D3DKMT_DESTROYCONTEXT
 - d3dkmthk/D3DKMT_DESTROYCONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmthk.h
api_name:
 - _D3DKMT_DESTROYCONTEXT
 - D3DKMT_DESTROYCONTEXT
---

# _D3DKMT_DESTROYCONTEXT structure


## -description

The D3DKMT_DESTROYCONTEXT structure contains a handle to a kernel-mode device context to release.

## -struct-fields

### -field hContext [in]

A handle to the device context that the Microsoft DirectX graphics kernel subsystem (<i>Dxgkrnl.sys</i>) supplied and that is returned from the call to the <a href="/windows-hardware/drivers/ddi/d3dkmthk/nf-d3dkmthk-d3dkmtcreatecontext">D3DKMTCreateContext</a> function.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmthk/nf-d3dkmthk-d3dkmtcreatecontext">D3DKMTCreateContext</a>



<a href="/windows-hardware/drivers/ddi/d3dkmthk/nf-d3dkmthk-d3dkmtdestroycontext">D3DKMTDestroyContext</a>

