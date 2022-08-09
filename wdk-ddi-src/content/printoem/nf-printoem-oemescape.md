---
UID: NF:printoem.OEMEscape
title: OEMEscape function (printoem.h)
description: The OEMEscape function retrieves information from a device that is not available in a device-independent device driver interface; the particular query depends on the value of the iEsc parameter.
tech.root: print
ms.date: 08/09/2022
keywords: ["OEMEscape function"]
ms.keywords: OEMEscape, OEMEscape function [Print Devices], print.oemescape, print_unidrv-pscript_rendering_6f5f3a3e-6027-4524-bb11-1010dfc48727.xml, printoem/OEMEscape
req.header: printoem.h
req.include-header: Printoem.h
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
req.typenames: 
f1_keywords:
 - OEMEscape
 - printoem/OEMEscape
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - OEMEscape
---

## -description

The **OEMEscape** function retrieves information from a device that is not available in a device-independent device driver interface; the particular query depends on the value of the *iEsc* parameter.

## -parameters

### -param pso

Defines the **SURFOBJ** parameter *pso*.

### -param iEsc

Defines the **ULONG** parameter *iEsc*.

### -param cjIn

Defines the **ULONG** parameter *cjIn*.

### -param pvIn [in]

Defines the **PVOID** parameter *pvIn*.

### -param cjOut

Defines the **ULONG** parameter *cjOut*.

### -param pvOut [out]

Defines the **PVOID** parameter *pvOut*.

## -returns

Returns a **ULONG** value.
