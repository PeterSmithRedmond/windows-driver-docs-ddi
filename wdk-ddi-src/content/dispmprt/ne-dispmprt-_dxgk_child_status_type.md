---
UID: NE:dispmprt._DXGK_CHILD_STATUS_TYPE
title: _DXGK_CHILD_STATUS_TYPE (dispmprt.h)
description: The DXGK_CHILD_STATUS_TYPE enumeration indicates the type of status being requested or reported for a child device of the display adapter.
old-location: display\dxgk_child_status_type.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["DXGK_CHILD_STATUS_TYPE enumeration"]
ms.keywords: "*PDXGK_CHILD_STATUS_TYPE, DXGK_CHILD_STATUS_TYPE, DXGK_CHILD_STATUS_TYPE enumeration [Display Devices], DmEnums_684c935e-6fd5-4743-a196-d6674b8f2e56.xml, PDXGK_CHILD_STATUS_TYPE, PDXGK_CHILD_STATUS_TYPE enumeration pointer [Display Devices], StatusConnection, StatusMiracast, StatusRotation, StatusUninitialized, _DXGK_CHILD_STATUS_TYPE, display.dxgk_child_status_type, dispmprt/DXGK_CHILD_STATUS_TYPE, dispmprt/PDXGK_CHILD_STATUS_TYPE, dispmprt/StatusConnection, dispmprt/StatusMiracast, dispmprt/StatusRotation, dispmprt/StatusUninitialized"
req.header: dispmprt.h
req.include-header: Dispmprt.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.typenames: DXGK_CHILD_STATUS_TYPE, *PDXGK_CHILD_STATUS_TYPE
f1_keywords:
 - _DXGK_CHILD_STATUS_TYPE
 - dispmprt/_DXGK_CHILD_STATUS_TYPE
 - PDXGK_CHILD_STATUS_TYPE
 - dispmprt/PDXGK_CHILD_STATUS_TYPE
 - DXGK_CHILD_STATUS_TYPE
 - dispmprt/DXGK_CHILD_STATUS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dispmprt.h
api_name:
 - _DXGK_CHILD_STATUS_TYPE
 - PDXGK_CHILD_STATUS_TYPE
 - DXGK_CHILD_STATUS_TYPE
---

# _DXGK_CHILD_STATUS_TYPE enumeration


## -description

The DXGK_CHILD_STATUS_TYPE enumeration indicates the type of status being requested or reported for a child device of the display adapter.

## -enum-fields

### -field StatusUninitialized

Indicates that a variable of type DXGK_CHILD_STATUS_TYPE has not yet been assigned a meaningful value.

### -field StatusConnection

Indicates that the request or report pertains to whether the child device has a monitor (or other display device) connected to it.

### -field StatusRotation

Indicates that the request or report pertains to the rotation angle of the monitor (or other display device) that is connected to the child device.

### -field StatusMiracastConnection

Indicates that the request or report pertains to a monitor (or other display device) that is connected wirelessly to the child device through a Miracast connected session.

Supported by WDDM 1.3 and later drivers running on Windows 8.1 and later.

## -remarks

The <b>Type</b> member of a <a href="/windows-hardware/drivers/ddi/dispmprt/ns-dispmprt-_dxgk_child_status">DXGK_CHILD_STATUS</a> structure is a member of the <b>DXGK_CHILD_STATUS_TYPE</b> enumeration.

## -see-also

<a href="/windows-hardware/drivers/ddi/dispmprt/nc-dispmprt-dxgkcb_indicate_child_status">DxgkCbIndicateChildStatus</a>



<a href="/windows-hardware/drivers/ddi/dispmprt/nc-dispmprt-dxgkddi_query_child_status">DxgkDdiQueryChildStatus</a>

