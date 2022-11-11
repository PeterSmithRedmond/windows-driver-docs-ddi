---
UID: NF:acxcircuit.AcxCircuitGetPinsCount
tech.root: audio
title: AcxCircuitGetPinsCount
ms.date: 11/09/2022
targetos: Windows
description: The AcxCircuitGetPinsCount function retrieves the number of pins for the specified circuit object.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxcircuit.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - acxcircuit.h
api_name:
 - AcxCircuitGetPinsCount
f1_keywords:
 - AcxCircuitGetPinsCount
 - acxcircuit/AcxCircuitGetPinsCount
dev_langs:
 - c++
helpviewer_keywords:
 - AcxCircuitGetPinsCount
---

## -description

The **AcxCircuitGetPinsCount** function retrieves the number of pins for the specified circuit object.

## -parameters

### -param Circuit [in]

The circuit object for which to get the number of pins.

## -returns

Returns the number of pins for the object specified by the *Circuit* parameter.

## -remarks

### ACX requirements

**Minimum ACX version:** 1.1

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [acxcircuit.h header](index.md)
