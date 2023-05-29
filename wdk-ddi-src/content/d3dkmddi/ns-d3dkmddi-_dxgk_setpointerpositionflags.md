---
UID: NS:d3dkmddi._DXGK_SETPOINTERPOSITIONFLAGS
title: DXGK_SETPOINTERPOSITIONFLAGS (d3dkmddi.h)
description: The DXGK_SETPOINTERPOSITIONFLAGS structure identifies, in bit-field flags, information about a mouse pointer.
old-location: display\dxgk_setpointerpositionflags.htm
ms.date: 12/09/2021
keywords: ["DXGK_SETPOINTERPOSITIONFLAGS structure"]
ms.keywords: DXGK_SETPOINTERPOSITIONFLAGS, DXGK_SETPOINTERPOSITIONFLAGS structure [Display Devices], DmStructs_57c5d8e6-b270-4423-8d85-5db8103e2492.xml, _DXGK_SETPOINTERPOSITIONFLAGS, d3dkmddi/DXGK_SETPOINTERPOSITIONFLAGS, display.dxgk_setpointerpositionflags
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
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
req.typenames: DXGK_SETPOINTERPOSITIONFLAGS
f1_keywords:
 - _DXGK_SETPOINTERPOSITIONFLAGS
 - d3dkmddi/_DXGK_SETPOINTERPOSITIONFLAGS
 - DXGK_SETPOINTERPOSITIONFLAGS
 - d3dkmddi/DXGK_SETPOINTERPOSITIONFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmddi.h
api_name:
 - _DXGK_SETPOINTERPOSITIONFLAGS
 - DXGK_SETPOINTERPOSITIONFLAGS
---

# DXGK_SETPOINTERPOSITIONFLAGS structure

## -description

The **DXGK_SETPOINTERPOSITIONFLAGS** structure identifies, in bit-field flags, information about a mouse pointer.

## -struct-fields

### -field Visible [in]

A **UINT** value that specifies whether the mouse pointer is visible. If this member is set, the mouse pointer is visible; if this member is not set, the mouse pointer is invisible. The driver should ignore the values in the **X** and **Y** members of the [**DXGKARG_SETPOINTERPOSITION**](ns-d3dkmddi-_dxgkarg_setpointerposition.md) structure if **Visible** is not set (that is, **Visible** is set to 0).

Setting this member is equivalent to setting the first bit of the 32-bit **Value** member (0x00000001).

### -field Procedural [in]

A **UINT** value that specifies whether the mouse pointer position was set by an application with the [**SetCursorPos**](/windows/win32/api/winuser/nf-winuser-setcursorpos) or similar cursor function instead of coming from user device input.

Setting this member is equivalent to setting the second bit of the 32-bit **Value** member (0x00000002).

Supported starting with Windows 8.

### -field Reserved [in]

This member is reserved and should be set to zero. Setting this member to zero is equivalent to setting remaining 30 bits (0xFFFFFFFC) of the 32-bit **Value** member to zeros.

### -field Value [in]

A member in the union that **DXGK_SETPOINTERPOSITIONFLAGS** contains that can hold one 32-bit value that indicates information about a mouse pointer.

## -see-also

[**DXGKARG_SETPOINTERPOSITION**](ns-d3dkmddi-_dxgkarg_setpointerposition.md)
