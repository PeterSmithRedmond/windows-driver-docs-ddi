---
UID: NF:acxcircuit.AcxCircuitInitSetCircuitType
tech.root: audio
title: AcxCircuitInitSetCircuitType
ms.date: 12/14/2022
targetos: Windows
description: The AcxCircuitInitSetCircuitType function is used to set the circuit type of the ACXCIRCUIT.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxcircuit.h
req.idl: 
req.include-header: 
req.irql: <= DISPATCH_LEVEL
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
 - AcxCircuitInitSetCircuitType
f1_keywords:
 - AcxCircuitInitSetCircuitType
 - acxcircuit/AcxCircuitInitSetCircuitType
dev_langs:
 - c++
---

## -description

The **AcxCircuitInitSetCircuitType** function is used to set the circuit type of the ACXCIRCUIT.

## -parameters

### -param CircuitInit

The ACXCIRCUIT_INIT structure that defines the circuit initialization. ACXCIRCUIT_INIT is an opaque object used for circuit initialization. Use [AcxCircuitInitAllocate](nf-acxcircuit-acxcircuitinitallocate.md) to initialize the ACXCIRCUIT_INIT structure.

### -param CircuitType

An [ACX_CIRCUIT_TYPE enum](ne-acxcircuit-acx_circuit_type.md) that is used to define the circuit type. For example, AcxCircuitTypeRender, AcxCircuitTypeCapture or AcxCircuitTypeOther.

## -remarks

### Example

Example usage is shown below.

```cpp
   ACX_CIRCUIT_TYPE                circuitType     = AcxCircuitTypeRender;

        // The driver uses this DDI to specify the circuit type. The
        // circuit type can be AcxCircuitTypeRender, AcxCircuitTypeCapture,
        // AcxCircuitTypeOther, or AcxCircuitTypeMaximum (for validation).
        //
        AcxCircuitInitSetCircuitType(circuitInit, AcxCircuitTypeRender);
```

### ACX requirements

**Minimum ACX version:** 1.0

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [acxcircuit.h header](index.md)
