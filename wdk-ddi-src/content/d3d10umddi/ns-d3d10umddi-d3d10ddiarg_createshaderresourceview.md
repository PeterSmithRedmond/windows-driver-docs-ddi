---
UID: NS:d3d10umddi.D3D10DDIARG_CREATESHADERRESOURCEVIEW
title: D3D10DDIARG_CREATESHADERRESOURCEVIEW (d3d10umddi.h)
description: The D3D10DDIARG_CREATESHADERRESOURCEVIEW structure describes the shader resource view to create.
old-location: display\d3d10ddiarg_createshaderresourceview.htm
ms.date: 11/03/2022
keywords: ["D3D10DDIARG_CREATESHADERRESOURCEVIEW structure"]
ms.keywords: D3D10DDIARG_CREATESHADERRESOURCEVIEW, D3D10DDIARG_CREATESHADERRESOURCEVIEW structure [Display Devices], UMDisplayDriver_Dx10param_Structs_5307f7f2-0e25-4847-b1d4-5300c27320b7.xml, d3d10umddi/D3D10DDIARG_CREATESHADERRESOURCEVIEW, display.d3d10ddiarg_createshaderresourceview
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
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
req.typenames: D3D10DDIARG_CREATESHADERRESOURCEVIEW
f1_keywords:
 - D3D10DDIARG_CREATESHADERRESOURCEVIEW
 - d3d10umddi/D3D10DDIARG_CREATESHADERRESOURCEVIEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10umddi.h
api_name:
 - D3D10DDIARG_CREATESHADERRESOURCEVIEW
---

# D3D10DDIARG_CREATESHADERRESOURCEVIEW structure

## -description

The **D3D10DDIARG_CREATESHADERRESOURCEVIEW** structure describes the shader resource view to create.

## -struct-fields

### -field hDrvResource [in]

A handle to the shader resource.

### -field Format [in]

A DXGI_FORMAT-typed value that indicates the pixel format of the view.

### -field ResourceDimension [in]

A [**D3D10DDIRESOURCE_TYPE**](/windows-hardware/drivers/display/ne-d3d10umddi-d3d10ddiresource_type)-typed value that indicates the resource type and dimensionality.

### -field Buffer [in]

If the value in the **ResourceDimension** member is set to D3D10DDIRESOURCE_BUFFER, a member in the union that is contained in D3D10DDIARG_CREATESHADERRESOURCEVIEW that can hold a [**D3D10DDIARG_BUFFER_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_buffer_shaderresourceview.md) structure for a buffer.

### -field Tex1D [in]

If the value in the **ResourceDimension** member is set to D3D10DDIRESOURCE_TEXTURE1D, a member in the union that is contained in D3D10DDIARG_CREATESHADERRESOURCEVIEW that can hold a [**D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_tex1d_shaderresourceview.md) structure for a one-dimensional texture.

### -field Tex2D [in]

If the value in the **ResourceDimension** member is set to D3D10DDIRESOURCE_TEXTURE2D, a member in the union that is contained in D3D10DDIARG_CREATESHADERRESOURCEVIEW that can hold a [**D3D10DDIARG_TEX2D_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_tex2d_shaderresourceview.md) structure for a two-dimensional texture.

### -field Tex3D [in]

If the value in the **ResourceDimension** member is set to D3D10DDIRESOURCE_TEXTURE3D, a member in the union that is contained in D3D10DDIARG_CREATESHADERRESOURCEVIEW that can hold a [**D3D10DDIARG_TEX3D_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_tex3d_shaderresourceview.md) structure for a three-dimensional texture.

### -field TexCube [in]

If the value in the **ResourceDimension** member is set to D3D10DDIRESOURCE_TEXTURECUBE, a member in the union that is contained in D3D10DDIARG_CREATESHADERRESOURCEVIEW that can hold a [**D3D10DDIARG_TEXCUBE_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_texcube_shaderresourceview.md) structure for a cube texture.

## -see-also

[**CalcPrivateShaderResourceViewSize**](nc-d3d10umddi-pfnd3d10ddi_calcprivateshaderresourceviewsize.md)

[**CreateShaderResourceView**](nc-d3d10umddi-pfnd3d10ddi_createshaderresourceview.md)

[**D3D10DDIARG_BUFFER_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_buffer_shaderresourceview.md)

[**D3D10DDIARG_TEX1D_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_tex1d_shaderresourceview.md)

[**D3D10DDIARG_TEX2D_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_tex2d_shaderresourceview.md)

[**D3D10DDIARG_TEX3D_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_tex3d_shaderresourceview.md)

[**D3D10DDIARG_TEXCUBE_SHADERRESOURCEVIEW**](ns-d3d10umddi-d3d10ddiarg_texcube_shaderresourceview.md)

[**D3D10DDIRESOURCE_TYPE**](/windows-hardware/drivers/display/ne-d3d10umddi-d3d10ddiresource_type)
