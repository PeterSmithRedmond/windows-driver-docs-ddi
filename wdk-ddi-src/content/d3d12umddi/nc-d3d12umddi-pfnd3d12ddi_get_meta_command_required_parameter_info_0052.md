---
UID: NC:d3d12umddi.PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052
title: PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052 (d3d12umddi.h)
description: Learn more about the PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052 callback function.
ms.date: 12/15/2023
keywords: ["PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052 callback function"]
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
 - PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052
 - d3d12umddi/PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052
dev_langs:
 - c++
---

# PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052 callback function

## -description

**PFND3D12DDI_GET_META_COMMAND_REQUIRED_PARAMETER_INFO_0052** gets required information for a meta-command.

## -parameters

### -param unnamedParam1

A handle to a meta-command.

### -param Stage

A pointer to a [**D3D12DDI_META_COMMAND_PARAMETER_STAGE**](ne-d3d12umddi-d3d12ddi_meta_command_parameter_stage.md).

### -param ParameterIndex

The index of the parameter.

### -param unnamedParam4

A pointer to a [**D3D12DDIARG_META_COMMAND_REQUIRED_PARAMETER_INFO**](ns-d3d12umddi-d3d12ddiarg_meta_command_required_parameter_info.md) structure in which the meta-command's required parameter info is written.

## -see-also

[D3D12DDI_META_COMMAND_PARAMETER_STAGE](ne-d3d12umddi-d3d12ddi_meta_command_parameter_stage.md)

[D3D12DDIARG_META_COMMAND_REQUIRED_PARAMETER_INFO](ns-d3d12umddi-d3d12ddiarg_meta_command_required_parameter_info.md)
