---
UID: NS:rilapitypes.RILUICCFILELOCKSTATUS
title: RILUICCFILELOCKSTATUS (rilapitypes.h)
description: "Microsoft reserves the RILUICCFILELOCKSTATUS structure for internal use only. Don't use this structure in your code."
old-location: netvista\riluiccfilelockstatus_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILUICCFILELOCKSTATUS structure"]
ms.keywords: "*LPRILUICCFILELOCKSTATUS, RILUICCFILELOCKSTATUS, RILUICCFILELOCKSTATUS structure [Network Drivers Starting with Windows Vista], netvista.riluiccfilelockstatus_2, rilapitypes/RILUICCFILELOCKSTATUS"
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
req.typenames: RILUICCFILELOCKSTATUS, *LPRILUICCFILELOCKSTATUS
f1_keywords:
 - RILUICCFILELOCKSTATUS
 - rilapitypes/RILUICCFILELOCKSTATUS
 - LPRILUICCFILELOCKSTATUS
 - rilapitypes/LPRILUICCFILELOCKSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILUICCFILELOCKSTATUS
 - LPRILUICCFILELOCKSTATUS
---

# RILUICCFILELOCKSTATUS structure (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -struct-fields

### -field cbSize

### -field dwParams

### -field dwAccessCondition

### -field bPinRef

## -syntax

```cpp
typedef struct _RILUICCFILELOCKSTATUS {
  DWORD                                 cbSize;
  DWORD                                 dwParams;
  RILUICCFILELOCKSTATUSACCESSCONDITION  dwAccessCondition;
  BYTE [MAXNUM_PINREF]                  bPinRef;
} RILUICCFILELOCKSTATUS, RILUICCFILELOCKSTATUS;
```

