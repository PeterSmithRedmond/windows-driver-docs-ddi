---
UID: NF:acxmisc.AcxObjectBagRetrieveI4
tech.root: audio
title: AcxObjectBagRetrieveI4
ms.date: 06/17/2022
targetos: Windows
description: The AcxObjectBagRetrieveI4 function retrieves a int four byte I4 (LONG) value from an existing, intialized AcxObjectBag that contains values.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxmisc.h
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
 - LibDef
api_location:
 - acxmisc.h
api_name:
 - AcxObjectBagRetrieveI4
f1_keywords:
 - AcxObjectBagRetrieveI4
 - acxmisc/AcxObjectBagRetrieveI4
dev_langs:
 - c++
---

## -description

The AcxObjectBagRetrieveI4 function retrieves a int four byte I4 (LONG) value from an existing, intialized AcxObjectBag that contains values.

## -parameters

### -param ObjectBag

An intialized ObjectBag ACX object. For more information, see [ACX - Summary of ACX Objects](/windows-hardware/drivers/audio/acx-summary-of-objects).

### -param ValueName

The name of the value that will be used to access the value.

### -param Value

The Value to be retrieved from the ObjectBag.

## -returns

Returns `STATUS_SUCCESS` if the call was successful. Otherwise, it returns an appropriate error code. For more information, see [Using NTSTATUS Values](/windows-hardware/drivers/kernel/using-ntstatus-values).

## -remarks

### Example

This example shows the use of AcxObjectBagRetrieveI4.

```cpp
    ACXOBJECTBAG objBag     = NULL;
    LONG         i4Value    = 0;

    //Initialize an object bag configuration
    ACX_OBJECTBAG_CONFIG objBagCfg;
    ACX_OBJECTBAG_CONFIG_INIT(&objBagCfg);
    
    // Set the WDF attributes, and create an object bag 
    WDF_OBJECT_ATTRIBUTES_INIT(&attributes);
    attributes.ParentObject = Circuit;
    RETURN_NTSTATUS_IF_FAILED(AcxObjectBagCreate(&attributes, &objBagCfg, &objBag));

    // Enable deletion of the object bag when the function completes and goes out of scope
    auto objBag_scope = scope_exit([&objBag]() {
        if (objBag != NULL)
        {
            WdfObjectDelete(objBag);
        }
    });

    //Create Properties and add them to an object bag
    DECLARE_CONST_ACXOBJECTBAG_DRIVER_PROPERTY_NAME(VendorX, TestI4);

    i4Value = 1;
    RETURN_NTSTATUS_IF_FAILED(AcxObjectBagAddI4(objBag, &TestI4, i4Value));

    // Retrieve the value from the object bag
    i4Value = 0;
    RETURN_NTSTATUS_IF_FAILED(AcxObjectBagRetrieveI4(objBag, &TestI4, &i4Value));
```

## -see-also

- [acxmisc.h header](index.md)
