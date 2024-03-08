---
UID: NC:d3dumddi.PFND3DDDI_SYNCTOKENCB
title: PFND3DDDI_SYNCTOKENCB (d3dumddi.h)
description: The PFND3DDDI_SYNCTOKENCB callback creates a sync token.
ms.date: 10/19/2018
keywords: ["PFND3DDDI_SYNCTOKENCB callback function"]
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
ms.custom: RS5
tech.root: display
f1_keywords:
 - PFND3DDDI_SYNCTOKENCB
 - d3dumddi/PFND3DDDI_SYNCTOKENCB
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3dumddi.h
api_name:
 - PFND3DDDI_SYNCTOKENCB
dev_langs:
 - c++
---

# PFND3DDDI_SYNCTOKENCB callback function


## -description

The PFND3DDDI_SYNCTOKENCB callback creates a sync token.

## -parameters

### -param hDevice

A handle to the graphics context device.

### -param unnamedParam2

Pointer to a [D3DDDICB_SYNCTOKEN](ns-d3dumddi-_d3dddicb_synctoken.md) structure.

## -returns

Returns HRESULT.

## -prototype

```cpp
//Declaration

PFND3DDDI_SYNCTOKENCB Pfnd3dddiSynctokencb; 

// Definition

HRESULT Pfnd3dddiSynctokencb 
(
	HANDLE hDevice
	 const D3DDDICB_SYNCTOKEN *
)
{...}

```

