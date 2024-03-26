---
UID: NS:rilapitypes.RILSUBSCRIBERINFO
title: RILSUBSCRIBERINFO (rilapitypes.h)
description: "Microsoft reserves the RILSUBSCRIBERINFO structure for internal use only. Don't use this structure in your code."
old-location: netvista\rilsubscriberinfo_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILSUBSCRIBERINFO structure"]
ms.keywords: "*LPRILSUBSCRIBERINFO, RILSUBSCRIBERINFO, RILSUBSCRIBERINFO structure [Network Drivers Starting with Windows Vista], netvista.rilsubscriberinfo_2, rilapitypes/RILSUBSCRIBERINFO"
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
req.typenames: RILSUBSCRIBERINFO, *LPRILSUBSCRIBERINFO
f1_keywords:
 - RILSUBSCRIBERINFO
 - rilapitypes/RILSUBSCRIBERINFO
 - LPRILSUBSCRIBERINFO
 - rilapitypes/LPRILSUBSCRIBERINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILSUBSCRIBERINFO
 - LPRILSUBSCRIBERINFO
---

# RILSUBSCRIBERINFO structure (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -struct-fields

### -field cbSize

### -field dwParams

### -field raAddress

### -field wszDescription

### -field dwService

## -syntax

```cpp
typedef struct _RILSUBSCRIBERINFO {
  DWORD                         cbSize;
  DWORD                         dwParams;
  RILADDRESS                    raAddress;
  WCHAR [MAXLENGTH_DESCRIPTION] wszDescription;
  RILSUBSCRIBERINFOSERVICE      dwService;
} RILSUBSCRIBERINFO, RILSUBSCRIBERINFO;
```

