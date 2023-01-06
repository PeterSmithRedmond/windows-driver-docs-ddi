---
UID: NF:acxcircuit.AcxFactoryCircuitGetSymbolicLinkName
tech.root: audio
title: AcxFactoryCircuitGetSymbolicLinkName
ms.date: 12/14/2022
targetos: Windows
description: The AcxFactoryCircuitGetSymbolicLinkName function retrieves the symbolic link name for the specified ACX factory circuit.
prerelease: false
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
 - AcxFactoryCircuitGetSymbolicLinkName
f1_keywords:
 - AcxFactoryCircuitGetSymbolicLinkName
 - acxcircuit/AcxFactoryCircuitGetSymbolicLinkName
dev_langs:
 - c++
helpviewer_keywords:
 - AcxFactoryCircuitGetSymbolicLinkName
---

## -description

The **AcxFactoryCircuitGetSymbolicLinkName** function retrieves the symbolic link name for the specified ACX factory circuit.

## -parameters

### -param Circuit [in]

The ACX factory circuit for which to retrieve the symbolic link name.

## -returns

Returns a string containing the symbolic link name for the ACX factory circuit object specified by the *Circuit* parameter.

## -remarks

The symbolic link is valid:

1. After the driver adds the circuit to the device, for single-circuit endpoints.
1. When the ACX manager invokes ACX circuit initialization, for multi-circuit endpoints.

### ACX requirements

**Minimum ACX version:** 1.1

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [acxcircuit.h header](index.md)
