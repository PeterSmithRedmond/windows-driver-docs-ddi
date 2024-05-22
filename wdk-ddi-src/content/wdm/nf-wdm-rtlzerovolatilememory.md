---
UID: NF:wdm.RtlZeroVolatileMemory
tech.root: kernel
title: RtlZeroVolatileMemory (wdm.h)
ms.date: 03/26/2024
targetos: Windows
description: Provides a convenience wrapper around RtlFillVolatileMemory.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll:
req.header: wdm.h
req.idl: 
req.include-header: Wdm.h
req.irql:
req.kmdf-ver: 
req.lib: volatileaccessk.lib (Kernel mode), volatileaccessu.lib (User mode)
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
 - wdm.h
api_name:
 - RtlZeroVolatileMemory
f1_keywords:
 - RtlZeroVolatileMemory
 - wdm/RtlZeroVolatileMemory
dev_langs:
 - c++
helpviewer_keywords:
 - RtlZeroVolatileMemory
---

## -description

The **RtlZeroVolatileMemory** function is a convenience wrapper around [**RtlFillVolatileMemory**](nf-wdm-rtlfillvolatilememory.md).

## -parameters

### -param Destination [out]

A pointer to the starting address of the block of memory to fill with zeros.

### -param Length [in]

The size of the block of memory to fill with zeros, in bytes.

## -returns

Returns the value of *Destination*.

## -remarks

The **RtlZeroVolatileMemory** function is a convenience wrapper around **RtlFillVolatileMemory**.

For more information, see the remarks section of [**RtlFillVolatileMemory**](nf-wdm-rtlfillvolatilememory.md).

> [!NOTE]
> This function works on all versions of Windows, not just the latest. You need to consume the latest WDK to get the function declaration from the wdm.h header. You also need the library (volatileaccessk.lib) from the latest WDK. However, the resulting driver will run fine on older versions of Windows.

### Example

```cpp
UCHAR SensitiveData[100];

// Imagine we temporarily store some sensitive cryptographic
// material in a buffer.

StoreCryptographicKey(&SensitiveData);
DoCryptographicOperation(&SensitiveData);

// Now that we are done using the sensitive data we want to
// erase it from the stack. We cannot call RtlFillMemory because
// if the compiler realizes that "SensitiveData" is not
// referenced again the compiler can remove the call to RtlFillMemory.
// Instead we can call RtlSecureZeroMemory2, RtlZeroVolatileMemory, or RtlFillVolatileMemory
// (the former two are convenience wrappers around the latter). These
// calls will not be optimized away by the compiler.
// Note that RtlSecureZeroMemory2 performs better than the
// RtlSecureZeroMemory function.

RtlZeroVolatileMemory(&SensitiveData, sizeof(SensitiveData));
```

## -see-also

[**RtlFillVolatileMemory**](nf-wdm-rtlfillvolatilememory.md)
