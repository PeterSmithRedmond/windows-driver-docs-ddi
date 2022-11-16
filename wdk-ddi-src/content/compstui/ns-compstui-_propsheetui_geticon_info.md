---
UID: NS:compstui._PROPSHEETUI_GETICON_INFO
title: PROPSHEETUI_GETICON_INFO (compstui.h)
description: The PROPSHEETUI_GETICON_INFO structure is used as an input parameter to an application's PFNPROPSHEETUI-typed function, when the function is called with a reason value of PROPSHEETUI_REASON_GET_ICON.
tech.root: print
ms.date: 11/16/2022
keywords: ["PROPSHEETUI_GETICON_INFO structure"]
ms.keywords: "*PPROPSHEETUI_GETICON_INFO, PPROPSHEETUI_GETICON_INFO, PPROPSHEETUI_GETICON_INFO structure pointer [Print Devices], PROPSHEETUI_GETICON_INFO, PROPSHEETUI_GETICON_INFO structure [Print Devices], _PROPSHEETUI_GETICON_INFO, compstui/PPROPSHEETUI_GETICON_INFO, compstui/PROPSHEETUI_GETICON_INFO, cpsuifnc_da228e66-0d1b-4d35-af1e-e1b99e56ad08.xml, print.propsheetui_geticon_info"
req.header: compstui.h
req.include-header: Compstui.h
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
req.typenames: PROPSHEETUI_GETICON_INFO, *PPROPSHEETUI_GETICON_INFO
f1_keywords:
 - _PROPSHEETUI_GETICON_INFO
 - compstui/_PROPSHEETUI_GETICON_INFO
 - PPROPSHEETUI_GETICON_INFO
 - compstui/PPROPSHEETUI_GETICON_INFO
 - PROPSHEETUI_GETICON_INFO
 - compstui/PROPSHEETUI_GETICON_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - compstui.h
api_name:
 - _PROPSHEETUI_GETICON_INFO
 - PPROPSHEETUI_GETICON_INFO
 - PROPSHEETUI_GETICON_INFO
---

## -description

The **PROPSHEETUI_GETICON_INFO** structure is used as an input parameter to an application's [PFNPROPSHEETUI](/windows-hardware/drivers/ddi/compstui/nc-compstui-pfnpropsheetui)-typed function, when the function is called with a reason value of PROPSHEETUI_REASON_GET_ICON.

## -struct-fields

### -field cbSize

CPSUI-supplied size, in bytes, of the **PROPSHEETUI_GETICON_INFO** structure.

### -field Flags

Reserved.

### -field cxIcon

CPSUI-supplied icon width, in pixels.

### -field cyIcon

CPSUI-supplied icon height, in pixels.

### -field hIcon

Receives an application-supplied icon handle. If the icon is not loaded, the member must be set to zero.
