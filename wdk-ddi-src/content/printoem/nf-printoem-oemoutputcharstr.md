---
UID: NF:printoem.OEMOutputCharStr
title: OEMOutputCharStr function (printoem.h)
description: This function (OEMOutputCharStr) is obsolete.
tech.root: print
ms.date: 08/12/2022
keywords: ["OEMOutputCharStr function"]
ms.keywords: OEMOutputCharStr, OEMOutputCharStr function [Print Devices], print.oemoutputcharstr, print_obsoletefunctions_250a623a-d7ce-48ba-9163-c24f52eb687d.xml, printoem/OEMOutputCharStr
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
 - OEMOutputCharStr
 - printoem/OEMOutputCharStr
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - OEMOutputCharStr
---

## -description

This function is obsolete for Windows XP and later. It is supported only for earlier Unidrv plug-ins.

Use [IPrintOemUni::OutputCharStr](../prcomoem/nf-prcomoem-iprintoemuni-outputcharstr.md) instead.

## -parameters

### -param pdevobj

Defines the **PDEVOBJ** parameter *pdevobj*.

### -param pUFObj

Defines the **PUNIFONTOBJ** parameter *pUFObj*.

### -param dwType

Defines the **DWORD** parameter *dwType*.

### -param dwCount

Defines the **DWORD** parameter *dwCount*.

### -param pGlyph [in]

Defines the **PVOID** parameter *pGlyph*.
