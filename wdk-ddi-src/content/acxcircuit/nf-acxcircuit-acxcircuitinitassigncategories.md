---
UID: NF:acxcircuit.AcxCircuitInitAssignCategories
tech.root: audio
title: AcxCircuitInitAssignCategories
ms.date: 12/14/2022
targetos: Windows
description: The AcxCircuitInitAssignCategories function assigns a set of KSCATERGORY entries for the ACXCIRCUIT.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxcircuit.h
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
 - HeaderDef
api_location:
 - acxcircuit.h
api_name:
 - AcxCircuitInitAssignCategories
f1_keywords:
 - AcxCircuitInitAssignCategories
 - acxcircuit/AcxCircuitInitAssignCategories
dev_langs:
 - c++
---

## -description

The **AcxCircuitInitAssignCategories** function assigns a set of KSCATERGORY entries for the ACXCIRCUIT.

## -parameters

### -param CircuitInit

The ACXCIRCUIT_INIT structure that defines the circuit initialization. ACXCIRCUIT_INIT is an opaque object used for circuit initialization. Use [AcxCircuitInitAllocate](nf-acxcircuit-acxcircuitinitallocate.md) to initialize the ACXCIRCUIT_INIT structure.

### -param Categories

An array that contains GUIDS of the desired KSCATERGORY, for example `KSCATEGORY_AUDIO`. For more information about the KSCATERGORY entries, see [Installing Device Interfaces for an Audio Adapter](/windows-hardware/drivers/audio/installing-device-interfaces-for-an-audio-adapter).

### -param CategoriesCount

The number of categories that will be added to the circuit. This is a one based count.

## -returns

Returns `STATUS_SUCCESS` if the call was successful. Otherwise, it returns an appropriate error code. For more information, see [Using NTSTATUS Values](/windows-hardware/drivers/kernel/using-ntstatus-values).

## -remarks

This call overrides the default category set initialized by ACX which is based on the ACXCIRCUIT type.

### Example

Example usage is shown below.

```cpp

    GUID captureCategories[] =
    {
        STATICGUIDOF(KSCATEGORY_AUDIO),
        STATICGUIDOF(KSCATEGORY_CAPTURE), 
        STATICGUIDOF(KSCATEGORY_REALTIME),
        STATICGUIDOF(KSCATEGORY_TOPOLOGY),
    };

    //
    // Add circuit identifiers.
    //
    AcxCircuitInitSetComponentId(CircuitInit, &COMPONENT_GUID);

    AcxCircuitInitAssignName(CircuitInit, &circuitName);

    status = AcxCircuitInitAssignCategories(CircuitInit, captureCategories, SIZEOF_ARRAY(captureCategories));
```

### ACX requirements

**Minimum ACX version:** 1.0

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [acxcircuit.h header](index.md)
