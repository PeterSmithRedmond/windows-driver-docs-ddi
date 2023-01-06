---
UID: NF:acxmisc.AcxObjectBagAddString
tech.root: audio
title: AcxObjectBagAddString
ms.date: 12/16/2022
targetos: Windows
description: The AcxObjectBagAddString function adds a WDFSTRING object to an existing, initialized AcxObjectBag.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxmisc.h
req.idl: 
req.include-header: 
req.irql: PASSIVE_LEVEL
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
 - LibDef
api_location:
 - acxmisc.h
api_name:
 - AcxObjectBagAddString
f1_keywords:
 - AcxObjectBagAddString
 - acxmisc/AcxObjectBagAddString
dev_langs:
 - c++
---

## -description

The AcxObjectBagAddString function adds a WDFSTRING object to an existing, initialized AcxObjectBag. For more information about WDFSTRING, see [wdfstring.h header](/windows-hardware/drivers/ddi/wdfstring/).

## -parameters

### -param ObjectBag

An initialized ObjectBag ACX object. For more information, see [ACX - Summary of ACX Objects](/windows-hardware/drivers/audio/acx-summary-of-objects).

### -param ValueName

A ValueName that will be associated with the added string and can be used to retrieve the stored string.

### -param Value

The value of the WDFSTRING object to be stored in the ObjectBag.

## -returns

Returns `STATUS_SUCCESS` if the call was successful. Otherwise, it returns an appropriate error code. For more information, see [Using NTSTATUS Values](/windows-hardware/drivers/kernel/using-ntstatus-values).

## -remarks

### ACX requirements

**Minimum ACX version:** 1.0

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [acxmisc.h header](index.md)
