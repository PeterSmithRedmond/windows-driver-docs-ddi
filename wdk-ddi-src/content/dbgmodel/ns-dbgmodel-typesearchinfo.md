---
UID: NS:dbgmodel.TypeSearchInfo
title: TypeSearchInfo (dbgmodel.h)
description: The TypeSearchInfo (dbgmodel.h) structure contains a search record passed to EnumerateChildrenEx specifically for SymbolType searches.
ms.date: 07/26/2023
keywords: ["TypeSearchInfo structure"]
ms.keywords: TypeSearchInfo, ,
req.header: dbgmodel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: 
targetos: Windows
tech.root: debugger
ms.custom: RS5
f1_keywords:
 - TypeSearchInfo
 - dbgmodel/TypeSearchInfo
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dbgmodel.h
api_name:
 - TypeSearchInfo
---

# TypeSearchInfo structure

## -description

The search record passed to EnumerateChildrenEx specifically for SymbolType searches.

## -struct-fields

### -field SearchType

Defines the type being searched for.

### -field SymbolSearchInfo

The the search record used to restrict symbol searches.

## -remarks

Use **SymbolSearchInfo** to describe the search record used to restrict symbol searches.

## -see-also

[Debugger Data Model C++ Overview](/windows-hardware/drivers/debugger/data-model-cpp-overview)
