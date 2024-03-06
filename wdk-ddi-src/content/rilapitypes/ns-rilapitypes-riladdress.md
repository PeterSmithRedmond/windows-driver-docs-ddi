---
UID: NS:rilapitypes.RILADDRESS
title: RILADDRESS (rilapitypes.h)
description: "Microsoft reserves the RILADDRESS structure for internal use only. Don't use this structure in your code."
old-location: netvista\riladdress_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILADDRESS structure"]
ms.keywords: "*LPRILADDRESS, RILADDRESS, RILADDRESS structure [Network Drivers Starting with Windows Vista], netvista.riladdress_2, rilapitypes/RILADDRESS"
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RILADDRESS, *LPRILADDRESS
f1_keywords:
 - RILADDRESS
 - rilapitypes/RILADDRESS
 - LPRILADDRESS
 - rilapitypes/LPRILADDRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILADDRESS
 - LPRILADDRESS
---

# RILADDRESS structure (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -struct-fields

### -field cbSize

### -field dwParams

### -field dwType

### -field dwNumPlan

### -field wszAddress

## -syntax

```cpp
typedef struct _RILADDRESS {
  DWORD                     cbSize;
  DWORD                     dwParams;
  RILADDRESSTYPE            dwType;
  RILADDRESSNUMPLAN         dwNumPlan;
  WCHAR [MAXLENGTH_ADDRESS] wszAddress;
} RILADDRESS, RILADDRESS;
```

