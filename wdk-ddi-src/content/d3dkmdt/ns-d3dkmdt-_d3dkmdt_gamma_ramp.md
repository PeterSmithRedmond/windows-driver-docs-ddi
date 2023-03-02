---
UID: NS:d3dkmdt._D3DKMDT_GAMMA_RAMP
title: D3DKMDT_GAMMA_RAMP (d3dkmdt.h)
description: The D3DKMDT_GAMMA_RAMP structure contains descriptive information about a gamma lookup table and a pointer to the lookup table.
old-location: display\d3dkmdt_gamma_ramp.htm
tech.root: display
ms.date: 02/28/2023
keywords: ["D3DKMDT_GAMMA_RAMP structure"]
ms.keywords: D3DKMDT_GAMMA_RAMP, D3DKMDT_GAMMA_RAMP structure [Display Devices], DmStructs_bb8721fc-b604-45e4-b3c8-ff27bda95e5b.xml, _D3DKMDT_GAMMA_RAMP, d3dkmdt/D3DKMDT_GAMMA_RAMP, display.d3dkmdt_gamma_ramp
req.header: d3dkmdt.h
req.include-header: 
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
req.typenames: D3DKMDT_GAMMA_RAMP
f1_keywords:
 - _D3DKMDT_GAMMA_RAMP
 - d3dkmdt/_D3DKMDT_GAMMA_RAMP
 - D3DKMDT_GAMMA_RAMP
 - d3dkmdt/D3DKMDT_GAMMA_RAMP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmdt.h
api_name:
 - _D3DKMDT_GAMMA_RAMP
 - D3DKMDT_GAMMA_RAMP
---

# D3DKMDT_GAMMA_RAMP structure

## -description

The **D3DKMDT_GAMMA_RAMP** structure contains descriptive information about a gamma lookup table and a pointer to the lookup table.

## -struct-fields

### -field Type

A [**D3DDDI_GAMMARAMP_TYPE**](../d3dukmdt/ne-d3dukmdt-_d3dddi_gammaramp_type.md) enumerator that specifies the format of the lookup table.

### -field DataSize

The size, in bytes, of the lookup table pointed to by **Data**.

### -field Data

[in] A union that contains one of the following ways to access the lookup table data depending on the value in the Type member:

### -field Data.pRgb256x3x16

If **Type** is equal to D3DDDI_GAMMARAMP_RGB256x3x16, this member is a pointer to a [**D3DDDI_GAMMA_RAMP_RGB256x3x16**](../d3dukmdt/ns-d3dukmdt-_d3dddi_gamma_ramp_rgb256x3x16.md) structure that contains the lookup table.

### -field Data.pDxgi1

If **Type** is equal to D3DDDI_GAMMARAMP_DXGI_1, this member is a pointer to a [**D3DDDI_GAMMA_RAMP_DXGI_1**](../d3dukmdt/ns-d3dukmdt-_d3dddi_gamma_ramp_dxgi_1.md) structure that contains the lookup table.

### -field Data.p3x4

If **Type** is D3DDDI_GAMMARAMP_MATRIX_3x4, this member is a pointer to a [**D3DDDI_3x4_COLORSPACE_TRANSFORM**](../d3dukmdt/ns-d3dukmdt-_d3dkmdt_3x4_colorspace_transform.md) structure which describes the 3 by 4 matrix color space transform to be applied, a scalar multiplier, and the lookup table. Available starting in WDDM 2.3.

### -field Data.pMatrixV2

If **Type** is equal to D3DDDI_GAMMARAMP_MATRIX_V2, this member is a pointer to a [**D3DKMDT_COLORSPACE_TRANSFORM_MATRIX_V2**](../d3dukmdt/ns-d3dukmdt-d3dkmdt_colorspace_transform_matrix_v2.md) structure that contains the lookup table. Available starting in WDDM 2.6.

### -field Data.pRaw

This member provides an alternative way to access the lookup table data. For example, for copying the lookup table, VOID* might be more convenient than D3DDDI_GAMMA_RAMP_RGB256x3x16.

## -remarks

The **GammaRamp** member of the [**D3DKMDT_VIDPN_PRESENT_PATH**](ns-d3dkmdt-_d3dkmdt_vidpn_present_path.md) structure is a D3DKMDT_GAMMA_RAMP structure.
