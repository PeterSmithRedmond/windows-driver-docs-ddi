---
UID: NS:dispmprt._DXGKARG_QUERYVIRTUALFUNCTIONLUID
title: _DXGKARG_QUERYVIRTUALFUNCTIONLUID
description: Arguments used to query virtual function LUID.
tech.root: display
ms.date: 04/04/2019
keywords: ["DXGKARG_QUERYVIRTUALFUNCTIONLUID structure"]
ms.keywords: _DXGKARG_QUERYVIRTUALFUNCTIONLUID, DXGKARG_QUERYVIRTUALFUNCTIONLUID, *PDXGKARG_QUERYVIRTUALFUNCTIONLUID,
req.header: dispmprt.h
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
req.typenames: DXGKARG_QUERYVIRTUALFUNCTIONLUID, *PDXGKARG_QUERYVIRTUALFUNCTIONLUID
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - _DXGKARG_QUERYVIRTUALFUNCTIONLUID
 - dispmprt/_DXGKARG_QUERYVIRTUALFUNCTIONLUID
 - PDXGKARG_QUERYVIRTUALFUNCTIONLUID
 - dispmprt/PDXGKARG_QUERYVIRTUALFUNCTIONLUID
 - DXGKARG_QUERYVIRTUALFUNCTIONLUID
 - dispmprt/DXGKARG_QUERYVIRTUALFUNCTIONLUID
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dispmprt.h
api_name:
 - _DXGKARG_QUERYVIRTUALFUNCTIONLUID
 - PDXGKARG_QUERYVIRTUALFUNCTIONLUID
 - DXGKARG_QUERYVIRTUALFUNCTIONLUID
dev_langs:
 - c++
---

# _DXGKARG_QUERYVIRTUALFUNCTIONLUID structure


## -description

Arguments used to query virtual function LUID.

## -struct-fields

### -field VirtualFunctionIndex

Zero-based offset of the Virtual Function from the first VF exposed by this Physical Function.

### -field pLuid

 
A pointer to a unique LUID that identifies a specific virtual GPU on the host system.

## -remarks

## -see-also

