---
UID: NF:printoem.OEMStartBanding
title: OEMStartBanding function (printoem.h)
description: The OEMStartBanding function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering.
tech.root: print
ms.date: 08/10/2022
keywords: ["OEMStartBanding function"]
ms.keywords: OEMStartBanding, OEMStartBanding function [Print Devices], print.oemstartbanding, print_unidrv-pscript_rendering_6738c42a-92b2-4360-ae4c-a4b474948667.xml, printoem/OEMStartBanding
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
 - OEMStartBanding
 - printoem/OEMStartBanding
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Printoem.h
api_name:
 - OEMStartBanding
---

## -description

The **OEMStartBanding** function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering.

## -parameters

### -param pso

Defines the **SURFOBJ** parameter *pso*.

### -param pptl

Defines the **POINTL** parameter *pptl*.

## -returns

Returns a **BOOL** value.
