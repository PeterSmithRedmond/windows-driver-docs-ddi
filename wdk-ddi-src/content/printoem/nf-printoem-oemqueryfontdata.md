---
UID: NF:printoem.OEMQueryFontData
title: OEMQueryFontData function (printoem.h)
description: The OEMQueryFontData function retrieves information about a realized font.
tech.root: print
ms.date: 08/10/2022
keywords: ["OEMQueryFontData function"]
ms.keywords: OEMQueryFontData, OEMQueryFontData function [Print Devices], print.oemqueryfontdata, print_unidrv-pscript_rendering_5044e745-e2bf-4047-a8d8-371fc21c33fa.xml, printoem/OEMQueryFontData
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
 - OEMQueryFontData
 - printoem/OEMQueryFontData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - OEMQueryFontData
---

## -description

The **OEMQueryFontData** function retrieves information about a realized font.

## -parameters

### -param dhpdev

Defines the **DHPDEV** parameter *dhpdev*.

### -param pfo

Defines the **FONTOBJ** parameter *pfo*.

### -param iMode

Defines the **ULONG** parameter *iMode*.

### -param hg

Defines the **HGLYPH** parameter *hg*.

### -param pgd

Defines the **GLYPHDATA** parameter *pgd*.

### -param pv [out]

Defines the **PVOID** parameter *pv*.

### -param cjSize

Defines the **ULONG** parameter *cjSize*.

## -returns

Returns a **LONG** value.
