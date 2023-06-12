---
UID: NS:d3dkmddi._DXGK_GDIARG_COLORFILL
title: DXGK_GDIARG_COLORFILL (d3dkmddi.h)
description: Learn more about the DXGK_GDIARG_COLORFILL structure.
ms.date: 06/09/2023
keywords: ["DXGK_GDIARG_COLORFILL structure"]
ms.keywords: DXGK_GDIARG_COLORFILL, DXGK_GDIARG_COLORFILL structure [Display Devices], DmStructs_d80a1a76-a7d1-4c7e-b9b1-3c6986124f77.xml, _DXGK_GDIARG_COLORFILL, d3dkmddi/DXGK_GDIARG_COLORFILL, display.dxgk_gdiarg_colorfill
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7
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
req.typenames: DXGK_GDIARG_COLORFILL
f1_keywords:
 - _DXGK_GDIARG_COLORFILL
 - d3dkmddi/_DXGK_GDIARG_COLORFILL
 - DXGK_GDIARG_COLORFILL
 - d3dkmddi/DXGK_GDIARG_COLORFILL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmddi.h
api_name:
 - _DXGK_GDIARG_COLORFILL
 - DXGK_GDIARG_COLORFILL
---

# DXGK_GDIARG_COLORFILL structure

## -description

The **DXGK_GDIARG_COLORFILL** structure describes the characteristics of a GDI hardware-accelerated color fill operation.

## -struct-fields

### -field DstRect [in]

A [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that defines the rectangular area to be modified. This rectangle is specified in the coordinate system of the destination surface and is defined by two points: upper left and lower right. The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the bit-block transfer. The two points that define the rectangle are always well ordered.

The destination rectangle defined by **DstRect** can exceed the bounds of the destination surface, but sub-rectangles cannot. Additionally, all sub-rectangles are guaranteed to fit inside the destination surface. Sub-rectangles can be constrained further by a bounding rectangle that is smaller than the destination rectangle.

### -field DstAllocationIndex

[in] An index of the element in the allocation list that specifies the allocation that is referenced by the **DstRect** destination rectangle.

### -field NumSubRects

[in] The number of sub-rectangles in the destination surface space. The sub-rectangles are not tightly bounded by the **DstRect** destination rectangle.

### -field pSubRects

[in] A pointer to the sub-rectangles in the destination surface space that is bounded by the **DstRect** destination rectangle.

### -field Color

[in] The fill color, in 32-bit ARGB unsigned pixel format (as defined by the D3DDDIFMT_A8R8G8B8 value of the [**D3DDDIFORMAT**](../d3dukmdt/ne-d3dukmdt-_d3dddiformat.md) enumeration).

### -field Rop

[in] An 8-bit value that specifies a GDI raster operation (ROP) that is defined by the constant values of the [**DXGK_GDIROP_COLORFILL**](ne-d3dkmddi-_dxgk_gdirop_colorfill.md) enumeration.

### -field Rop3

[in] An 8-bit value that specifies a ternary GDI raster operation (ROP3) that combines a brush, a source bitmap, and a destination bitmap in one of 256 possible combinations. This type of raster operation will be processed only if the driver has set the **SupportAllBltRops** member in the [**DXGK_PRESENTATIONCAPS**](ns-d3dkmddi-_dxgk_presentationcaps.md) structure.

## -see-also

[**D3DDDIFORMAT**](../d3dukmdt/ne-d3dukmdt-_d3dddiformat.md)

[**DXGK_GDIROP_COLORFILL**](ne-d3dkmddi-_dxgk_gdirop_colorfill.md)

[**DXGK_PRESENTATIONCAPS**](ns-d3dkmddi-_dxgk_presentationcaps.md)

[**RECT**](/windows/win32/api/windef/ns-windef-rect)
