---
UID: NC:d3d12umddi.PFND3D12DDI_CREATE_COMMAND_LIST_0040
title: PFND3D12DDI_CREATE_COMMAND_LIST_0040 (d3d12umddi.h)
description: Pointer to the CreateCommandList function that creates a command list.
ms.date: 10/19/2018
keywords: ["PFND3D12DDI_CREATE_COMMAND_LIST_0040 callback function"]
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
f1_keywords:
 - PFND3D12DDI_CREATE_COMMAND_LIST_0040
 - d3d12umddi/PFND3D12DDI_CREATE_COMMAND_LIST_0040
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_CREATE_COMMAND_LIST_0040
---

# PFND3D12DDI_CREATE_COMMAND_LIST_0040 callback function


## -description

Pointer to the CreateCommandList function that creates a command list.

## -parameters

### -param unnamedParam1

A handle to the display device (graphics context).

### -param unnamedParam2

Pointer to a D3D12DDIARG_CREATE_COMMAND_LIST_0040 structure that describes the parameters that the user-mode display driver uses to create a command list.

### -param unnamedParam3

A handle to the driver's data for the command list. The driver uses this region of memory to store internal data structures that are related to its command list.

### -param unnamedParam4

A handle to the command list that the driver should use, when it calls back into the Direct3D runtime.

## -returns

Returns an HRESULT.

## -prototype

```cpp
//Declaration

PFND3D12DDI_CREATE_COMMAND_LIST_0040 Pfnd3d12ddiCreateCommandList0040;

// Definition

HRESULT Pfnd3d12ddiCreateCommandList0040
(
	 D3D12DDI_HDEVICE
	CONST D3D12DDIARG_CREATE_COMMAND_LIST_0040 *
	 D3D12DDI_HCOMMANDLIST
	 D3D12DDI_HRTCOMMANDLIST
)
{...}

PFND3D12DDI_CREATE_COMMAND_LIST_0040


```

## -remarks

## -see-also

