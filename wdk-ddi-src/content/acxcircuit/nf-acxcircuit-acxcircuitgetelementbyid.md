---
UID: NF:acxcircuit.AcxCircuitGetElementById
tech.root: audio
title: AcxCircuitGetElementById
ms.date: 04/27/2022
targetos: Windows
description: When provided a valid ElementID number, the AcxCircuitGetElementById function returns the corresponding ACXELEMENT object.
prerelease: true
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
 - AcxCircuitGetElementById
f1_keywords:
 - AcxCircuitGetElementById
 - acxcircuit/AcxCircuitGetElementById
dev_langs:
 - c++
---

## -description

When provided a valid ElementID number, the **AcxCircuitGetElementById** function returns the corresponding ACXELEMENT object. For more information about ACX objects, see [Summary of ACX Objects](/windows-hardware/drivers/audio/acx-summary-of-objects).

## -parameters

### -param Circuit

An existing ACXCIRCUIT object.

### -param ElementId

A valid Element ID number.

## -returns

The requested ACXELEMENT object associated with the provided element ID number.  

## -remarks

### Example

Example usage is shown below.

```cpp
    ACXELEMENT              element     = nullptr;
    ULONGLONG               index       = GetMessageContext(Event); // Context is an index.

    element = AcxCircuitGetElementById(Circuit, (ULONG)index);
```

### ACX requirements

**Minimum ACX version:** 1.0

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [acxcircuit.h header](index.md)

