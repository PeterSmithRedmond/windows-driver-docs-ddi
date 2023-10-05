---
UID: NS:d3dkmthk._D3DKMT_GETPRESENTHISTORY
title: _D3DKMT_GETPRESENTHISTORY (d3dkmthk.h)
description: The D3DKMT_GETPRESENTHISTORY structure describes the state of copying history.
old-location: display\d3dkmt_getpresenthistory.htm
ms.date: 05/10/2018
keywords: ["D3DKMT_GETPRESENTHISTORY structure"]
ms.keywords: D3DKMT_GETPRESENTHISTORY, D3DKMT_GETPRESENTHISTORY structure [Display Devices], OpenGL_Structs_966946a8-3611-4c25-a57f-1fc99c2004d0.xml, _D3DKMT_GETPRESENTHISTORY, d3dkmthk/D3DKMT_GETPRESENTHISTORY, display.d3dkmt_getpresenthistory
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
req.typenames: D3DKMT_GETPRESENTHISTORY
f1_keywords:
 - _D3DKMT_GETPRESENTHISTORY
 - d3dkmthk/_D3DKMT_GETPRESENTHISTORY
 - D3DKMT_GETPRESENTHISTORY
 - d3dkmthk/D3DKMT_GETPRESENTHISTORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmthk.h
api_name:
 - _D3DKMT_GETPRESENTHISTORY
 - D3DKMT_GETPRESENTHISTORY
---

# _D3DKMT_GETPRESENTHISTORY structure


## -description

The D3DKMT_GETPRESENTHISTORY structure describes the state of copying history.

## -struct-fields

### -field hAdapter [in]

The handle to the graphics adapter.

### -field ProvidedSize [in]

Supported in Windows 7 and later versions.

The size, in bytes, of the provided buffer that the <b>pTokens</b> member points to.

### -field WrittenSize [out]

Supported in Windows 7 and later versions.

The size, in bytes, that the <a href="/windows-hardware/drivers/ddi/d3dkmthk/nf-d3dkmthk-d3dkmtgetpresenthistory">D3DKMTGetPresentHistory</a> function copies to the buffer that the <b>pTokens</b> member points to or the required size for first token.

### -field pTokens [in/out]

Supported in Windows 7 and later versions.

A pointer to the buffer that receives the tokens. Each token is described by a <a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_presenthistorytoken">D3DKMT_PRESENTHISTORYTOKEN</a> structure.

### -field NumTokens [out]

Supported in Windows 7 and later versions.

The number of tokens that the <a href="/windows-hardware/drivers/ddi/d3dkmthk/nf-d3dkmthk-d3dkmtgetpresenthistory">D3DKMTGetPresentHistory</a> function copies to the buffer that the <b>pTokens</b> member points to.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmthk/nf-d3dkmthk-d3dkmtgetpresenthistory">D3DKMTGetPresentHistory</a>



<a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_presenthistorytoken">D3DKMT_PRESENTHISTORYTOKEN</a>

