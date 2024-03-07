---
UID: NC:d3d12umddi.PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB
title: PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB (d3d12umddi.h)
description: Sets the command list table.
ms.date: 10/19/2018
keywords: ["PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB callback function"]
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
 - PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB
 - d3d12umddi/PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB
dev_langs:
 - c++
---

# PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB callback function


## -description

Sets the command list table.

## -parameters

### -param unnamedParam1

A handle to a command list.

### -param unnamedParam2

A handle to a table.

## -prototype

```cpp
//Declaration

PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB Pfnd3d12ddiSetcommandlistdditableCb;

// Definition

VOID Pfnd3d12ddiSetcommandlistdditableCb
(
	 D3D12DDI_HRTCOMMANDLIST
	 D3D12DDI_HRTTABLE
)
{...}

PFND3D12DDI_SETCOMMANDLISTDDITABLE_CB


```

