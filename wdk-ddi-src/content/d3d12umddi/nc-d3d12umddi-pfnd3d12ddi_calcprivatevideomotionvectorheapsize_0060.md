---
UID: NC:d3d12umddi.PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060
title: PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060
description: The PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060 callback function calculates the video motion vector heap size.
tech.root: display
ms.date: 04/04/2019
keywords: ["PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060 callback function"]
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1903
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: UMD DDI Min Version D3D12DDI_SUPPORTED_0043, 19H1
f1_keywords:
 - PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060
 - d3d12umddi/PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060
dev_langs:
 - c++
---

# PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060 callback function


## -description

Calculates the video motion vector heap size.

## -parameters

### -param hDrvDevice

A handle to the display device (graphics context).

### -param pArgs

Pointer to a [D3D12DDIARG_CREATE_VIDEO_MOTION_VECTOR_HEAP_0060](ns-d3d12umddi-d3d12ddiarg_create_video_motion_vector_heap_0060.md) structure.

## -returns

Returns SIZE_T.

## -prototype

```
//Declaration

PFND3D12DDI_CALCPRIVATEVIDEOMOTIONVECTORHEAPSIZE_0060 Pfnd3d12ddiCalcprivatevideomotionvectorheapsize0060; 

// Definition

SIZE_T Pfnd3d12ddiCalcprivatevideomotionvectorheapsize0060 
(
	D3D12DDI_HDEVICE hDrvDevice
	 const D3D12DDIARG_CREATE_VIDEO_MOTION_VECTOR_HEAP_0060 *pArgs
)
{...}

```

## -remarks

## -see-also

