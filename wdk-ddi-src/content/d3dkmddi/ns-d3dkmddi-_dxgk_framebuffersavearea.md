---
UID: NS:d3dkmddi._DXGK_FRAMEBUFFERSAVEAREA
title: DXGK_FRAMEBUFFERSAVEAREA (d3dkmddi.h)
description: The DXGK_FRAMEBUFFERSAVEAREA structure specifies the size required by the driver to save the frame buffer reserve area during power transitions.
ms.date: 07/22/2021
keywords: ["DXGK_FRAMEBUFFERSAVEAREA structure"]
ms.keywords: _DXGK_FRAMEBUFFERSAVEAREA, DXGK_FRAMEBUFFERSAVEAREA,
req.header: d3dkmddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: DXGK_FRAMEBUFFERSAVEAREA
targetos: Windows
tech.root: display
f1_keywords:
 - _DXGK_FRAMEBUFFERSAVEAREA
 - d3dkmddi/_DXGK_FRAMEBUFFERSAVEAREA
 - DXGK_FRAMEBUFFERSAVEAREA
 - d3dkmddi/DXGK_FRAMEBUFFERSAVEAREA
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3dkmddi.h
api_name:
 - _DXGK_FRAMEBUFFERSAVEAREA
 - DXGK_FRAMEBUFFERSAVEAREA
---

# DXGK_FRAMEBUFFERSAVEAREA structure

## -description

The **DXGK_FRAMEBUFFERSAVEAREA** structure specifies the size required by the driver to save the frame buffer reserve area during power transitions.

## -struct-fields

### -field MaximumSize

The maximum size required by the driver to save the frame buffer reserve area during power transitions. This value must be a multiple of PAGE_SIZE.

## -remarks

See [IOMMU-based GPU isolation](/windows-hardware/drivers/display/iommu-based-gpu-isolation) for more information.

## -see-also

[**DXGKDDI_QUERYADAPTERINFO**](nc-d3dkmddi-dxgkddi_queryadapterinfo.md)

[**DXGKQAITYPE_FRAMEBUFFERSAVESIZE**](ne-d3dkmddi-_dxgk_queryadapterinfotype.md)
