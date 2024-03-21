---
UID: NC:d3d12umddi.PFND3D12DDI_CREATE_SHADER_0010
title: PFND3D12DDI_CREATE_SHADER_0010 (d3d12umddi.h)
description: The PFND3D12DDI_CREATE_SHADER_0010 callback function creates a display device shader.
ms.date: 10/19/2018
keywords: ["PFND3D12DDI_CREATE_SHADER_0010 callback function"]
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
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
tech.root: display
ms.custom: RS5
f1_keywords:
 - PFND3D12DDI_CREATE_SHADER_0010
 - d3d12umddi/PFND3D12DDI_CREATE_SHADER_0010
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_CREATE_SHADER_0010
dev_langs:
 - c++
---

# PFND3D12DDI_CREATE_SHADER_0010 callback function


## -description

Create shader.

## -parameters

### -param unnamedParam1

A handle to the display device (graphics context).

### -param unnamedParam2

Pointer to a D3D12DDIARG_CREATE_SHADER_0010 structure.

### -param unnamedParam3

Shader handle.

## -prototype

```cpp
//Declaration

PFND3D12DDI_CREATE_SHADER_0010 Pfnd3d12ddiCreateShader0010; 

// Definition

VOID Pfnd3d12ddiCreateShader0010 
(
	 D3D12DDI_HDEVICE
	CONST D3D12DDIARG_CREATE_SHADER_0010 *
	 D3D12DDI_HSHADER
)
{...}

PFND3D12DDI_CREATE_SHADER_0010 


```

