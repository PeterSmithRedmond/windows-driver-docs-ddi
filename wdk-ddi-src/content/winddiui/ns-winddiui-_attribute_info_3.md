---
UID: NS:winddiui._ATTRIBUTE_INFO_3
title: ATTRIBUTE_INFO_3 (winddiui.h)
description: The ATTRIBUTE_INFO_3 structure is used as a parameter for a printer interface DLL's DrvQueryJobAttributes function. All member values are function-supplied.
tech.root: print
ms.date: 03/09/2023
keywords: ["ATTRIBUTE_INFO_3 structure"]
ms.keywords: "*PATTRIBUTE_INFO_3, ATTRIBUTE_INFO_3, ATTRIBUTE_INFO_3 structure [Print Devices], PATTRIBUTE_INFO_3, PATTRIBUTE_INFO_3 structure pointer [Print Devices], _ATTRIBUTE_INFO_3, print.attribute_info_3, print_interface-graphics_473dca69-31fc-410d-a9d6-cfa5241f2c5b.xml, winddiui/ATTRIBUTE_INFO_3, winddiui/PATTRIBUTE_INFO_3"
req.header: winddiui.h
req.include-header: Winddiui.h, Winsplp.h
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
req.typenames: ATTRIBUTE_INFO_3, *PATTRIBUTE_INFO_3
f1_keywords:
 - _ATTRIBUTE_INFO_3
 - winddiui/_ATTRIBUTE_INFO_3
 - PATTRIBUTE_INFO_3
 - winddiui/PATTRIBUTE_INFO_3
 - ATTRIBUTE_INFO_3
 - winddiui/ATTRIBUTE_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddiui.h
api_name:
 - _ATTRIBUTE_INFO_3
 - PATTRIBUTE_INFO_3
 - ATTRIBUTE_INFO_3
---

## -description

The ATTRIBUTE_INFO_3 structure is used as a parameter for a printer interface DLL's [DrvQueryJobAttributes](/windows-hardware/drivers/ddi/winddiui/nf-winddiui-drvqueryjobattributes) function. All member values are function-supplied.

## -struct-fields

### -field dwJobNumberOfPagesPerSide

Number of document pages to be placed on one side of a physical page, as requested by the user. Allowable values are 1, 2, 4, 6, 9, or 16.

### -field dwDrvNumberOfPagesPerSide

Number of document pages that the printer and driver can place on one side of a physical page. This value must be 1 or the value specified for **dwJobNumberOfPagesPerSide**.

### -field dwNupBorderFlags

One of the following bit flag values:

| Flag | Definition |
|---|---|
| BORDER_PRINT | The print processor should draw a border around the page. |
| NO_BORDER_PRINT | The print processor should not draw a border around the page. |

### -field dwJobPageOrderFlags

One of the following bit flag values:

| Flag | Definition |
|---|---|
| BOOKLET_PRINT | Pages should be printed in booklet form, with two document pages printed on one side of a physical page. In landscape mode, the two document pages are printed side-by-side on the paper. In portrait mode, the two document pages are printed top-and-bottom. |
| NORMAL_PRINT | Pages should be printed in normal order: page 1, page 2, and so on. |
| REVERSE_PRINT | Pages should be printed in reverse order: last page, next-to-last page, and so on. |

### -field dwDrvPageOrderFlags

Bit flags indicating which page ordering options are supported by the printer and driver. Uses the same flags as **dwJobPageOrderFlags**.

### -field dwJobNumberOfCopies

Number of copies of the print job, as requested by the user.

### -field dwDrvNumberOfCopies

Maximum number of copies the printer and driver can handle at once, taking into account such job attributes as collating and stapling.

### -field dwColorOptimization

One of the following bit flag values:

| Flag | Definition |
|---|---|
| COLOR_OPTIMIZATION | The print processor should use monochrome color optimization. |
| NO_COLOR_OPTIMIZATION | The print processor should not use monochrome color optimization. |

### -field dmPrintQuality

Value to be used instead of the **dmPrintQuality** member of the print job's [**DEVMODEW**](/windows/win32/api/wingdi/ns-wingdi-devmodew) structure, if the COLOR_OPTIMIZATION flag is set in **dwColorOptimization**.

### -field dmYResolution

Value to be used instead of the **dmYResolution** member of the print job's DEVMODEW structure, if the COLOR_OPTIMIZATION flag is set in **dwColorOptimization**.

## -remarks

If the **dmPrintQuality** member of a print job's DEVMODEW structure is a negative value, such as DMRES_HIGH, and if monochrome color optimization is enabled, then switching between color and monochrome could result in different resolutions being used. This is because DMRES_HIGH might be assigned to different DPI values for color and monochrome rendering. (For Unidrv-supported devices, this assignment occurs in the printer's [GPD](/windows-hardware/drivers/) file.) To ensure a consistent resolution throughout the print job, the driver can specify positive **dmPrintQuality** and **dmYResolution** values (representing a specific DPI resolution) to override the equivalent [**DEVMODEW**](/windows/win32/api/wingdi/ns-wingdi-devmodew) values.

The EMF print processor uses the flag specified for **dwColorOptimization** to determine whether to request GDI to perform monochrome color optimization. If monochrome color optimization is enabled, the print job can be switched between monochrome and color rendering as appropriate.

If you are creating a Unidrv rendering plug-in to generate color watermarks, note that when the **dwColorOptimization** member is set to COLOR_OPTIMIZATION, color watermarks are printed in black and white when they are printed on black-and-white documents. To ensure that color watermarks print correctly with color and black-and-white documents, disable color optimization. Color optimization also can be controlled by the Unidrv ***ChangeColorModeOnDoc?** color attribute (see [Color Attributes](/windows-hardware/drivers/print/color-attributes)), and by the [GdiEndPageEMF](/windows-hardware/drivers/ddi/winppi/nf-winppi-gdiendpageemf) function.

For information about other ATTRIBUTE_INFO_3 structure members, see [**ATTRIBUTE_INFO_1**](/windows-hardware/drivers/ddi/winddiui/ns-winddiui-_attribute_info_1) and [**ATTRIBUTE_INFO_2**](/windows-hardware/drivers/ddi/winddiui/ns-winddiui-_attribute_info_2).

## -see-also

[**ATTRIBUTE_INFO_2**](/windows-hardware/drivers/ddi/winddiui/ns-winddiui-_attribute_info_2)

[**ATTRIBUTE_INFO_4**](/windows-hardware/drivers/ddi/winddiui/ns-winddiui-_attribute_info_4)

[DrvQueryJobAttributes](/windows-hardware/drivers/ddi/winddiui/nf-winddiui-drvqueryjobattributes)

[GdiEndPageEMF](/windows-hardware/drivers/ddi/winppi/nf-winppi-gdiendpageemf)

[GetJobAttributesEx](/windows-hardware/drivers/ddi/winsplp/nf-winsplp-getjobattributesex)
