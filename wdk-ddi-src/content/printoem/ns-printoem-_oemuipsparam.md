---
UID: NS:printoem._OEMUIPSPARAM
title: OEMUIPSPARAM (printoem.h)
description: The OEMUIPSPARAM structure is passed to a user interface plug-in's IPrintOemUI::DevicePropertySheets and IPrintOemUI::DocumentPropertySheets methods.
tech.root: print
ms.date: 08/12/2022
keywords: ["OEMUIPSPARAM structure"]
ms.keywords: "*POEMUIPSPARAM, OEMUIPSPARAM, OEMUIPSPARAM structure [Print Devices], POEMUIPSPARAM, POEMUIPSPARAM structure pointer [Print Devices], _OEMUIPSPARAM, print.oemuipsparam, print_unidrv-pscript_ui_7a4c3f10-5a2d-45da-99e4-bbd6ee0fb8bf.xml, printoem/OEMUIPSPARAM, printoem/POEMUIPSPARAM"
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
req.typenames: OEMUIPSPARAM, *POEMUIPSPARAM
f1_keywords:
 - _OEMUIPSPARAM
 - printoem/_OEMUIPSPARAM
 - POEMUIPSPARAM
 - printoem/POEMUIPSPARAM
 - OEMUIPSPARAM
 - printoem/OEMUIPSPARAM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - _OEMUIPSPARAM
 - POEMUIPSPARAM
 - OEMUIPSPARAM
---

## -description

The **OEMUIPSPARAM** structure is passed to a user interface plug-in's [IPrintOemUI::DevicePropertySheets](/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemui-devicepropertysheets) and [IPrintOemUI::DocumentPropertySheets](/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemui-documentpropertysheets) methods.

## -struct-fields

### -field cbSize

Size of the **OEMUIPSPARAM** structure. Supplied by the Unidrv or Pscript5 driver.

### -field poemuiobj

Not used.

### -field hPrinter

Handle to the printer. Supplied by the Unidrv or Pscript5 driver.

### -field pPrinterName

String containing the printer name. Supplied by the Unidrv or Pscript5 driver.

### -field hModule

Handle to the user interface plug-in. Supplied by the Unidrv or Pscript5 driver.

### -field hOEMHeap

Handle to a heap from which space can be allocated by calling the **HeapAlloc** function. Supplied by the Unidrv or Pscript5 driver.

### -field pPublicDM

#### For calls to IPrintOemUI::DocumentPropertySheets

Caller-supplied pointer to the printer's public **DEVMODEW** structure.

#### For calls to IPrintOemUI::DevicePropertySheets

Not used.

### -field pOEMDM

**For calls to IPrintOemUI::DocumentPropertySheets**  
Caller-supplied pointer to the user interface plug-in's private **DEVMODEW** members.

**For calls to IPrintOemUI::DevicePropertySheets**  
Not used.

### -field pOEMUserData

Pointer, supplied by user interface plug-in, to a location containing private information. This pointer is returned to the plug-in's [_CPSUICALLBACK](/windows-hardware/drivers/ddi/compstui/nc-compstui-_cpsuicallback)-typed callback function when a property sheet item has changed.

### -field dwFlags

**For calls to IPrintOemUI::DocumentPropertySheets**  
Contains the contents of the **fMode** member of the **DOCUMENTPROPERTYHEADER** structure received by the printer driver's [DrvDocumentPropertySheets](/windows-hardware/drivers/ddi/winddiui/nf-winddiui-drvdocumentpropertysheets) function.

**For calls to IPrintOemUI::DevicePropertySheets**  
Contains the contents of the **Flags** member of the **DEVICEPROPERTYHEADER** structure received by the printer driver's [DrvDevicePropertySheets](/windows-hardware/drivers/ddi/winddiui/nf-winddiui-drvdevicepropertysheets) function.

### -field pOemEntry

Reserved for system use.

## -see-also

[DrvDevicePropertySheets](/windows-hardware/drivers/ddi/winddiui/nf-winddiui-drvdevicepropertysheets)

[DrvDocumentPropertySheets](/windows-hardware/drivers/ddi/winddiui/nf-winddiui-drvdocumentpropertysheets)

[IPrintOemUI::DevicePropertySheets](/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemui-devicepropertysheets)

[IPrintOemUI::DocumentPropertySheets](/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemui-documentpropertysheets)

[_CPSUICALLBACK](/windows-hardware/drivers/ddi/compstui/nc-compstui-_cpsuicallback)
