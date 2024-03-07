---
UID: NC:d3d12umddi.PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013
title: PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013 (d3d12umddi.h)
description: "The PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013 callback function calculates the driver's root signature size."
tech.root: display
ms.date: 11/28/2018
keywords: ["PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013 callback function"]
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10
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
f1_keywords:
 - PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013
 - d3d12umddi/PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013
---

# PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013 callback function


## -description

Calculates the driver's root signature size.

## -parameters

### -param unnamedParam1

A handle to the display device (graphics context).

### -param unnamedParam2

Pointer to a D3D12DDIARG_CREATE_ROOT_SIGNATURE_0013 structure.

## -returns

Returns SIZE_T.

## -prototype

```
//Declaration

PFND3D12DDI_CALC_PRIVATE_ROOT_SIGNATURE_SIZE_0013 Pfnd3d12ddiCalcPrivateRootSignatureSize0013; 

// Definition

SIZE_T Pfnd3d12ddiCalcPrivateRootSignatureSize0013 
(
	D3D12DDI_HDEVICE Arg1
	 const D3D12DDIARG_CREATE_ROOT_SIGNATURE_0013 *
)
{...}

```

## -remarks

## -see-also

