---
UID: NF:printoem.OEMRealizeBrush
title: OEMRealizeBrush function (printoem.h)
description: The OEMRealizeBrush function requests that the driver realize a specified brush for a specified surface.
tech.root: print
ms.date: 08/10/2022
keywords: ["OEMRealizeBrush function"]
ms.keywords: OEMRealizeBrush, OEMRealizeBrush function [Print Devices], print.oemrealizebrush, print_unidrv-pscript_rendering_ab4f8635-9dda-4f08-b4f9-d70681ec532e.xml, printoem/OEMRealizeBrush
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
 - OEMRealizeBrush
 - printoem/OEMRealizeBrush
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - OEMRealizeBrush
---

## -description

The **OEMRealizeBrush** function requests that the driver realize a specified brush for a specified surface.

## -parameters

### -param pbo

Defines the **BRUSHOBJ** parameter *pbo*.

### -param psoTarget

Defines the **SURFOBJ** parameter *psoTarget*.

### -param psoPattern

Defines the **SURFOBJ** parameter *psoPattern*.

### -param psoMask

Defines the **SURFOBJ** parameter *psoMask*.

### -param pxlo

Defines the **XLATEOBJ** parameter *pxlo*.

### -param iHatch

Defines the **ULONG** parameter *iHatch*.

## -returns

Returns a **BOOL** value.
