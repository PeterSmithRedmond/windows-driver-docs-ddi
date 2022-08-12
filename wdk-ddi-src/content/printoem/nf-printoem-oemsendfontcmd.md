---
UID: NF:printoem.OEMSendFontCmd
title: OEMSendFontCmd function (printoem.h)
description: This function (OEMSendFontCmdSW) is obsolete.
tech.root: print
ms.date: 08/12/2022
keywords: ["OEMSendFontCmd function"]
ms.keywords: OEMSendFontCmd, OEMSendFontCmd function [Print Devices], print.oemsendfontcmd, print_obsoletefunctions_f54bf949-57eb-49ea-a69b-f9edfdfb9da6.xml, printoem/OEMSendFontCmd
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
 - OEMSendFontCmd
 - printoem/OEMSendFontCmd
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - OEMSendFontCmd
---

## -description

This function is obsolete for Windows XP and later. It is supported only for earlier Unidrv plug-ins.

Use [IPrintOemUni::SendFontCmd](../prcomoem/nf-prcomoem-iprintoemuni-sendfontcmd.md) instead.

## -parameters

### -param pdevobj

Defines the **PDEVOBJ** parameter *pdevobj*.

### -param pUFObj

Defines the **PUNIFONTOBJ** parameter *pUFObj*.

### -param pFInv

Defines the **PFINVOCATION** parameter *pFInv*.
