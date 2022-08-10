---
UID: NF:printoem.OEMNextBand
title: OEMNextBand function (printoem.h)
description: The OEMNextBand function is called by GDI when it has finished drawing a band for a physical page, so that the driver can send the band to the printer.
tech.root: print
ms.date: 08/10/2022
keywords: ["OEMNextBand function"]
ms.keywords: OEMNextBand, OEMNextBand function [Print Devices], print.oemnextband, print_unidrv-pscript_rendering_db168f2e-09ab-4c1d-9a68-970af445e128.xml, printoem/OEMNextBand
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
 - OEMNextBand
 - printoem/OEMNextBand
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - OEMNextBand
---

## -description

The **OEMNextBand** function is called by GDI when it has finished drawing a band for a physical page, so that the driver can send the band to the printer.

## -parameters

### -param pso

Defines the **SURFOBJ** parameter *pso*.

### -param pptl

Defines the **POINTL** parameter *pptl*.

## -returns

Returns a **BOOL** value.
