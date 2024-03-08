---
UID: NC:d3dumddi.PFND3DDDI_QUERYDLISTFORAPPLICATION
title: PFND3DDDI_QUERYDLISTFORAPPLICATION (d3dumddi.h)
description: The PFND3DDDI_QUERYDLISTFORAPPLICATION callback function queries a DList for an application.
ms.date: 10/19/2018
keywords: ["PFND3DDDI_QUERYDLISTFORAPPLICATION callback function"]
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
 - PFND3DDDI_QUERYDLISTFORAPPLICATION
 - d3dumddi/PFND3DDDI_QUERYDLISTFORAPPLICATION
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3dumddi.h
api_name:
 - PFND3DDDI_QUERYDLISTFORAPPLICATION
dev_langs:
 - c++
---

# PFND3DDDI_QUERYDLISTFORAPPLICATION callback function


## -description

The PFND3DDDI_QUERYDLISTFORAPPLICATION callback function queries a DList for an application.

## -parameters

### -param unnamedParam1 [out]

Indicates whether or not there is an application in the DList.

## -returns

Returns HRESULT.

## -prototype

```cpp
//Declaration

PFND3DDDI_QUERYDLISTFORAPPLICATION Pfnd3dddiQuerydlistforapplication; 

// Definition

HRESULT Pfnd3dddiQuerydlistforapplication 
(
	BOOL *
)
{...}

```

