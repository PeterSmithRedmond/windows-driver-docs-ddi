---
UID: NF:ks.KsGenerateThermalEvent
title: KsGenerateThermalEvent function (ks.h)
description: This function is used by clients (miniport drivers) that do not want to subscribe to the thermal manager, but want to do their own thermal management.
tech.root: stream
ms.date: 11/11/2022
keywords: ["KsGenerateThermalEvent function"]
ms.keywords: KsGenerateThermalEvent, KsGenerateThermalEvent function [Streaming Media Devices], ks/KsGenerateThermalEvent, stream.ksgeneratethermalevent
req.header: ks.h
req.include-header: 
req.target-type: Universal
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
req.lib: Ks.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - KsGenerateThermalEvent
 - ks/KsGenerateThermalEvent
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ks.lib
 - ks.dll
api_name:
 - KsGenerateThermalEvent
---

## -description

This function is used by clients (miniport drivers) that do not want to subscribe to the thermal manager, but want to do their own thermal management.

There is a check that verifies whether the miniport driver has the query interface support for a thermal manager (for example, the device is actively managed by a thermal manager). In cases of devices managed by a thermal manager, this call is rejected.

## -parameters

### -param Object [in]

Can be [**KSDEVICE**](/windows-hardware/drivers/ddi/ks/ns-ks-_ksdevice), [**KSFILTER**](/windows-hardware/drivers/ddi/ks/ns-ks-_ksfilter), or [**KSPIN**](/windows-hardware/drivers/ddi/ks/ns-ks-_kspin). Depending on the object passed, the thermal notification is sent device-wide, filter-wide, or to the pin.

### -param Value [in]

KSDEVICE_THERMAL_STATE_LOW or KSDEVICE_THERMAL_STATE_HIGH

## -returns

 Returns STATUS_SUCCESS for success and STATUS_INVALID_DEVICE_REQUEST if the parameters are incorrect.
