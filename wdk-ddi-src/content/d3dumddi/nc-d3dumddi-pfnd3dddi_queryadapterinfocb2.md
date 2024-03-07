---
UID: NC:d3dumddi.PFND3DDDI_QUERYADAPTERINFOCB2
title: PFND3DDDI_QUERYADAPTERINFOCB2 (d3dumddi.h)
description: Implemented by the client driver to retrieve graphics adapter information.
ms.date: 10/19/2018
keywords: ["PFND3DDDI_QUERYADAPTERINFOCB2 callback function"]
req.header: d3dumddi.h
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
 - PFND3DDDI_QUERYADAPTERINFOCB2
 - d3dumddi/PFND3DDDI_QUERYADAPTERINFOCB2
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3dumddi.h
api_name:
 - PFND3DDDI_QUERYADAPTERINFOCB2
---

# PFND3DDDI_QUERYADAPTERINFOCB2 callback function


## -description

Implemented by the client driver to retrieve graphics adapter information.

## -parameters

### -param hAdapter

A handle to the graphics adapter object.

### -param unnamedParam2

A pointer to a [D3DDDICB_QUERYADAPTERINFO2](ns-d3dumddi-_d3dddicb_queryadapterinfo2.md) structure that receives information about the graphics hardware.

## -returns

<b>pfnQueryAdapterInfoCb2</b> returns one of the following values:

|Return code|Description|
|--|--|
|S_OK|Information was successfully retrieved.|
|E_INVALIDARG|Parameters were validated and determined to be incorrect.|


This function might also return other HRESULT values.

## -prototype

```cpp
//Declaration

PFND3DDDI_QUERYADAPTERINFOCB2 Pfnd3dddiQueryadapterinfocb2;

// Definition

HRESULT Pfnd3dddiQueryadapterinfocb2
(
	HANDLE hAdapter
	CONST D3DDDICB_QUERYADAPTERINFO2 *
)
{...}

PFND3DDDI_QUERYADAPTERINFOCB2


```

