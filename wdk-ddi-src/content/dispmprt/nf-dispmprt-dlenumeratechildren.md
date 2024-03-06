---
UID: NF:dispmprt.DlEnumerateChildren
title: DlEnumerateChildren function
description: Allows a miniport driver to force a re-enumeration of its child devices.
tech.root: display
ms.date: 04/04/2019
keywords: ["DlEnumerateChildren function"]
ms.keywords: DlEnumerateChildren
req.header: dispmprt.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - DlEnumerateChildren
 - dispmprt/DlEnumerateChildren
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Displib.lib
 - Displib.dll
api_name:
 - DlEnumerateChildren
dev_langs:
 - c++
---

# DlEnumerateChildren function


## -description

Allows a miniport driver to force a re-enumeration of its child devices.

## -parameters

### -param DeviceHandle

Pointer to a device handle.

### -param Reserved

Reserved.

## -returns

This function returns VP_STATUS.

## -remarks

## -see-also

