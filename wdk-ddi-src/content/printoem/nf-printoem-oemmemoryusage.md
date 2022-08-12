---
UID: NF:printoem.OEMMemoryUsage
title: OEMMemoryUsage function (printoem.h)
description: This function (OEMMemoryUsage) is obsolete.
tech.root: print
ms.date: 08/12/2022
keywords: ["OEMMemoryUsage function"]
ms.keywords: OEMMemoryUsage, OEMMemoryUsage function [Print Devices], print.oemmemoryusage__function_, print_obsoletefunctions_35165216-4a29-4096-95b6-5f5b00418193.xml, printoem/OEMMemoryUsage
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
 - OEMMemoryUsage
 - printoem/OEMMemoryUsage
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - OEMMemoryUsage
---

## -description

This function is obsolete for Windows XP and later. It is supported only for earlier Unidrv plug-ins.

Use [IPrintOemUni::MemoryUsage](../prcomoem/nf-prcomoem-iprintoemuni-memoryusage.md) instead.

## -parameters

### -param pdevobj

Pointer to device object.

### -param pMemoryUsage [in, out]

Pointer to OEMMEMORYUSAGE structure.
