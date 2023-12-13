---
UID: NS:d3d12umddi.D3D12DDIARG_META_COMMAND_DESC
title: D3D12DDIARG_META_COMMAND_DESC (d3d12umddi.h)
description: Learn more about the D3D12DDIARG_META_COMMAND_DESC structure.
ms.date: 12/12/2023
keywords: ["D3D12DDIARG_META_COMMAND_DESC structure"]
ms.keywords: D3D12DDIARG_META_COMMAND_DESC, D3D12DDIARG_META_COMMAND_DESC,
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1809
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12DDIARG_META_COMMAND_DESC
targetos: Windows
tech.root: display
ms.custom: RS5
f1_keywords:
 - D3D12DDIARG_META_COMMAND_DESC
 - d3d12umddi/D3D12DDIARG_META_COMMAND_DESC
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12umddi.h
api_name:
 - D3D12DDIARG_META_COMMAND_DESC
dev_langs:
 - c++
---

# D3D12DDIARG_META_COMMAND_DESC structure

## -description

The **D3D12DDIARG_META_COMMAND_DESC** structure contains the description of a meta-command. A meta-command is a Direct3D object intended to represent an IHV-accelerated algorithm. It’s an opaque reference to a command generator implemented by the driver.

## -struct-fields

### -field Id

The id of a meta-command.

### -field Name

Pointer to a wide string that holds the name of the meta-command. The driver allocates and keeps this string for the lifetime of the device.

### -field InitializationDirtyState

A [**D3D12DDI_GRAPHICS_STATES**](ne-d3d12umddi-d3d12ddi_graphics_states.md) value specifying the command list states that are modified by the initialization call.

### -field ExecutionDirtyState

A [**D3D12DDI_GRAPHICS_STATES**](ne-d3d12umddi-d3d12ddi_graphics_states.md) value specifying the command list states that are modified by the execute call.

## -remarks

## -see-also

[**PFND3D12DDI_ENUMERATE_META_COMMANDS_0052**](nc-d3d12umddi-pfnd3d12ddi_enumerate_meta_commands_0052.md)