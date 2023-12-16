---
UID: NC:d3d12umddi.PFND3D12DDI_CREATE_META_COMMAND_0052
title: PFND3D12DDI_CREATE_META_COMMAND_0052 (d3d12umddi.h)
description: Learn more about the PFND3D12DDI_CREATE_META_COMMAND_0052 callback function.
ms.date: 12/15/2023
keywords: ["PFND3D12DDI_CREATE_META_COMMAND_0052 callback function"]
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1809
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
 - PFND3D12DDI_CREATE_META_COMMAND_0052
 - d3d12umddi/PFND3D12DDI_CREATE_META_COMMAND_0052
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_CREATE_META_COMMAND_0052
product:
 - Windows
dev_langs:
 - c++
---

# PFND3D12DDI_CREATE_META_COMMAND_0052 callback function

## -description

Creates a meta-command.

## -parameters

### -param unnamedParam1

A handle to the display device (graphics context).

### -param CommandId

The command id.

### -param NodeMask

The node mask of the command list.

### -param pCreationParameters

The creation parameters.

### -param CreationParametersDataSizeInBytes

The size of the creation parameters.

### -param unnamedParam6

Handle to a meta-command.

### -param unnamedParam7

A meta-command.

## -returns

Returns HRESULT.

## -prototype

```cpp
//Declaration

PFND3D12DDI_CREATE_META_COMMAND_0052 Pfnd3d12ddiCreateMetaCommand0052; 

// Definition

HRESULT Pfnd3d12ddiCreateMetaCommand0052 
(
	D3D12DDI_HDEVICE Arg1
	GUID CommandId
	UINT NodeMask
	CONST void *pCreationParameters
	SIZE_T CreationParametersDataSizeInBytes
	D3D12DDI_HMETACOMMAND_0052 Arg2
	D3D12DDI_HRTMETACOMMAND_0052 Arg3
)
{...}

```

## -remarks

The runtime will validate the meta-command guid via an approved list. This check can only be bypassed in developer mode. Without this only predefined meta-commands are allowed. All predefined meta-commands have a defined spec and HLK tests to validate their functionality.

## -see-also

[**PFND3D12DDI_DESTROY_META_COMMAND_0052**](nc-d3d12umddi-pfnd3d12ddi_destroy_meta_command_0052.md)

[**PFND3D12DDI_EXECUTE_META_COMMAND_0052**](nc-d3d12umddi-pfnd3d12ddi_execute_meta_command_0052.md)

[**PFND3D12DDI_INITIALIZE_META_COMMAND_0052**](nc-d3d12umddi-pfnd3d12ddi_initialize_meta_command_0052.md)
