---
UID: NE:iddcx.IDDCX_MONITOR_MODE_ORIGIN
title: IDDCX_MONITOR_MODE_ORIGIN (iddcx.h)
description: Used to describe a mode the monitor supports based on the monitor description.
old-location: display\iddcx_monitor_mode_origin.htm
tech.root: display
ms.date: 08/08/2022
keywords: ["IDDCX_MONITOR_MODE_ORIGIN enumeration"]
ms.keywords: IDDCX_MONITOR_MODE_ORIGIN, IDDCX_MONITOR_MODE_ORIGIN enumeration [Display Devices], IDDCX_MONITOR_MODE_ORIGIN_DRIVER, IDDCX_MONITOR_MODE_ORIGIN_MONITORDESCRIPTOR, IDDCX_MONITOR_MODE_ORIGIN_UNINITIALIZED, display.iddcx_monitor_mode_origin, iddcx/IDDCX_MONITOR_MODE_ORIGIN, iddcx/IDDCX_MONITOR_MODE_ORIGIN_DRIVER, iddcx/IDDCX_MONITOR_MODE_ORIGIN_MONITORDESCRIPTOR, iddcx/IDDCX_MONITOR_MODE_ORIGIN_UNINITIALIZED
req.header: iddcx.h
req.include-header: 
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
 - IDDCX_MONITOR_MODE_ORIGIN
 - iddcx/IDDCX_MONITOR_MODE_ORIGIN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iddcx.h
api_name:
 - IDDCX_MONITOR_MODE_ORIGIN
---

# IDDCX_MONITOR_MODE_ORIGIN enumeration

## -description

A **IDDCX_MONITOR_MODE_ORIGIN** value describes a mode the monitor supports based on the monitor description.

## -enum-fields

### -field IDDCX_MONITOR_MODE_ORIGIN_UNINITIALIZED:0

Indicates that an **IDDCX_MONITOR_MODE_ORIGIN** variable has not yet been assigned a meaningful value.

### -field IDDCX_MONITOR_MODE_ORIGIN_MONITORDESCRIPTOR:1

Indicates that the driver added this mode from directly processing the monitor description.

### -field IDDCX_MONITOR_MODE_ORIGIN_DRIVER:2

Indicates that the driver did not add this mode as a direct resolution of processing the modes/ supported by the monitor but because of separate additional knowledge it has about the monitor.

## -see-also

[**IDDCX_MONITOR_MODE**](ns-iddcx-iddcx_monitor_mode.md)
