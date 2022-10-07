---
UID: NC:d3dkmthk.PDXGK_GRAPHICSPOWER_UNREGISTER
title: PDXGK_GRAPHICSPOWER_UNREGISTER (d3dkmthk.h)
description: A callback to un-register itself with the graphics driver.
old-location: display\pdxgk_graphicspower_unregister.htm
ms.date: 10/07/2022
keywords: ["PDXGK_GRAPHICSPOWER_UNREGISTER callback function"]
ms.keywords: PDXGK_GRAPHICSPOWER_UNREGISTER, PDXGK_GRAPHICSPOWER_UNREGISTER callback, PDXGK_GRAPHICSPOWER_UNREGISTER callback function [Display Devices], d3dkmthk/PDXGK_GRAPHICSPOWER_UNREGISTER, display.pdxgk_graphicspower_unregister
req.header: d3dkmthk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.irql: <= APC_LEVEL
targetos: Windows
tech.root: display
ms.custom: engagement-fy23
req.typenames: 
f1_keywords:
 - PDXGK_GRAPHICSPOWER_UNREGISTER
 - d3dkmthk/PDXGK_GRAPHICSPOWER_UNREGISTER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - d3dkmthk.h
api_name:
 - PDXGK_GRAPHICSPOWER_UNREGISTER
---

# PDXGK_GRAPHICSPOWER_UNREGISTER callback function

## -description

A callback to un-register itself with the graphics driver.

## -parameters

### -param DeviceHandle

An opaque handle which should be provided when making callbacks to the graphics device.

### -param PrivateHandle

An opaque handle which will be provided in any callbacks. This handle must be globally unique, therefore, a pointer to the calling driver’s PDO or FDO should be used.

## -returns

Return STATUS_SUCCESS if the call succeeds.
