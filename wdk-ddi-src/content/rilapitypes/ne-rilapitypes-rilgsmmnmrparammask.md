---
UID: NE:rilapitypes.RILGSMMNMRPARAMMASK
title: RILGSMMNMRPARAMMASK (rilapitypes.h)
description: "Microsoft reserves the RILGSMMNMRPARAMMASK enumeration for internal use only. Don't use this enumeration in your code."
old-location: netvista\rilgsmmnmrparammask_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILGSMMNMRPARAMMASK enumeration"]
ms.keywords: RILGSMMNMRPARAMMASK, RILGSMMNMRPARAMMASK enumeration [Network Drivers Starting with Windows Vista], RIL_PARAM_GSMNMR_ALL, RIL_PARAM_GSMNMR_ARFCN, RIL_PARAM_GSMNMR_BSID, RIL_PARAM_GSMNMR_CELLID, RIL_PARAM_GSMNMR_LAC, RIL_PARAM_GSMNMR_MNC, RIL_PARAM_GSMNMR_RXLEVEL, netvista.rilgsmmnmrparammask_2, rilapitypes/RILGSMMNMRPARAMMASK, rilapitypes/RIL_PARAM_GSMNMR_ALL, rilapitypes/RIL_PARAM_GSMNMR_ARFCN, rilapitypes/RIL_PARAM_GSMNMR_BSID, rilapitypes/RIL_PARAM_GSMNMR_CELLID, rilapitypes/RIL_PARAM_GSMNMR_LAC, rilapitypes/RIL_PARAM_GSMNMR_MNC, rilapitypes/RIL_PARAM_GSMNMR_RXLEVEL
req.header: rilapitypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RILGSMMNMRPARAMMASK
f1_keywords:
 - RILGSMMNMRPARAMMASK
 - rilapitypes/RILGSMMNMRPARAMMASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILGSMMNMRPARAMMASK
---

# RILGSMMNMRPARAMMASK enumeration (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -enum-fields

### -field RIL_PARAM_GSMNMR_MCC

### -field RIL_PARAM_GSMNMR_MNC

### -field RIL_PARAM_GSMNMR_LAC

### -field RIL_PARAM_GSMNMR_CELLID

### -field RIL_PARAM_GSMNMR_ARFCN

### -field RIL_PARAM_GSMNMR_BSID

### -field RIL_PARAM_GSMNMR_RXLEVEL

### -field RIL_PARAM_GSMNMR_ALL

## -syntax

```cpp
typedef enum _RILGSMMNMRPARAMMASK {
  RIL_PARAM_GSMNMR_MNC,
  RIL_PARAM_GSMNMR_LAC,
  RIL_PARAM_GSMNMR_CELLID,
  RIL_PARAM_GSMNMR_ARFCN,
  RIL_PARAM_GSMNMR_BSID,
  RIL_PARAM_GSMNMR_RXLEVEL,
  RIL_PARAM_GSMNMR_ALL
} RILGSMMNMRPARAMMASK;
```

