---
UID: NS:winddiui._DEVICEPROPERTYHEADER
title: _DEVICEPROPERTYHEADER (winddiui.h)
description: The DEVICEPROPERTYHEADER structure is used as an input parameter to a printer interface DLL's DrvDevicePropertySheets function.
tech.root: print
ms.date: 03/09/2023
keywords: ["DEVICEPROPERTYHEADER structure"]
ms.keywords: "*PDEVICEPROPERTYHEADER, DEVICEPROPERTYHEADER, DEVICEPROPERTYHEADER structure [Print Devices], PDEVICEPROPERTYHEADER, PDEVICEPROPERTYHEADER structure pointer [Print Devices], _DEVICEPROPERTYHEADER, print.devicepropertyheader, print_interface-graphics_7dc4be04-e0ab-43bb-8e6d-f500cc7cf51c.xml, winddiui/DEVICEPROPERTYHEADER, winddiui/PDEVICEPROPERTYHEADER"
req.header: winddiui.h
req.include-header: Winddiui.h
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
req.typenames: DEVICEPROPERTYHEADER, *PDEVICEPROPERTYHEADER
f1_keywords:
 - _DEVICEPROPERTYHEADER
 - winddiui/_DEVICEPROPERTYHEADER
 - PDEVICEPROPERTYHEADER
 - winddiui/PDEVICEPROPERTYHEADER
 - DEVICEPROPERTYHEADER
 - winddiui/DEVICEPROPERTYHEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddiui.h
api_name:
 - _DEVICEPROPERTYHEADER
 - PDEVICEPROPERTYHEADER
 - DEVICEPROPERTYHEADER
---

## -description

The **DEVICEPROPERTYHEADER** structure is used as an input parameter to a printer interface DLL's [DrvDevicePropertySheets](./nf-winddiui-drvdevicepropertysheets.md) function.

## -struct-fields

### -field cbSize

Size, in bytes, of the **DEVICEPROPERTYHEADER** structure.

### -field Flags

Is a set of flags that can be set to the following value:

| Value | Meaning |
|---|---|
| DPS_NOPERMISSION | If set, the user is not permitted to update device settings. |

### -field hPrinter

Printer handle.

### -field pszPrinterName

Pointer to a NULL-terminated string representing a printer name.