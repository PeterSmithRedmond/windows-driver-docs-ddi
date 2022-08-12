---
UID: NS:printoem._PDEV_ADJUST_GRAPHICS_RESOLUTION
title: PDEV_ADJUST_GRAPHICS_RESOLUTION (printoem.h)
description: The PDEV_ADJUST_GRAPHICS_RESOLUTION structure specifies a graphics resolution value.
tech.root: print
ms.date: 08/12/2022
keywords: ["PDEV_ADJUST_GRAPHICS_RESOLUTION structure"]
ms.keywords: "*PPDEV_ADJUST_GRAPHICS_RESOLUTION, PDEV_ADJUST_GRAPHICS_RESOLUTION, PDEV_ADJUST_GRAPHICS_RESOLUTION structure [Print Devices], PPDEV_ADJUST_GRAPHICS_RESOLUTION, PPDEV_ADJUST_GRAPHICS_RESOLUTION structure pointer [Print Devices], _PDEV_ADJUST_GRAPHICS_RESOLUTION, print.pdev_adjust_graphics_resolution, print_unidrv-pscript_rendering_4e6d42c6-744c-4451-85a3-f5769c0ebfd3.xml, printoem/PDEV_ADJUST_GRAPHICS_RESOLUTION, printoem/PPDEV_ADJUST_GRAPHICS_RESOLUTION"
req.header: printoem.h
req.include-header: Printoem.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: PDEV_ADJUST_GRAPHICS_RESOLUTION, *PPDEV_ADJUST_GRAPHICS_RESOLUTION
f1_keywords:
 - _PDEV_ADJUST_GRAPHICS_RESOLUTION
 - printoem/_PDEV_ADJUST_GRAPHICS_RESOLUTION
 - PPDEV_ADJUST_GRAPHICS_RESOLUTION
 - printoem/PPDEV_ADJUST_GRAPHICS_RESOLUTION
 - PDEV_ADJUST_GRAPHICS_RESOLUTION
 - printoem/PDEV_ADJUST_GRAPHICS_RESOLUTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - _PDEV_ADJUST_GRAPHICS_RESOLUTION
 - PPDEV_ADJUST_GRAPHICS_RESOLUTION
 - PDEV_ADJUST_GRAPHICS_RESOLUTION
---

## -description

The **PDEV_ADJUST_GRAPHICS_RESOLUTION** structure specifies a graphics resolution value.

## -struct-fields

### -field ptGraphicsResolution

A **POINT** structure that specifies the resolution of the graphics area, in dots per inch (DPI).

## -remarks

The **PDEV_ADJUST_GRAPHICS_RESOLUTION** structure is available in Windows Vista and later operating systems.
