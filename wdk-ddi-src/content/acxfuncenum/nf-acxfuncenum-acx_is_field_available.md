---
UID: NF:acxfuncenum.ACX_IS_FIELD_AVAILABLE
tech.root: audio
title: ACX_IS_FIELD_AVAILABLE
ms.date: 09/23/2022
targetos: Windows
description: The ACX_IS_FIELD_AVAILABLE function enables you to query if the specified field is available in the specified ACX structure on the system.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxfuncenum.h
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
 - acxfuncenum.h
api_name:
 - ACX_IS_FIELD_AVAILABLE
f1_keywords:
 - ACX_IS_FIELD_AVAILABLE
 - acxfuncenum/ACX_IS_FIELD_AVAILABLE
dev_langs:
 - c++
helpviewer_keywords:
 - ACX_IS_FIELD_AVAILABLE
---

## -description

The **ACX_IS_FIELD_AVAILABLE** function enables you to query if the specified field is available in the specified ACX structure on the system.

## -parameters

### -param StructName

The name of the ACX structure that contains the field specified in the *FieldName* parameter.

### -param FieldName

The name of the field to query in the ACX structure specified in the *StructName* parameter.

## -remarks

Returns TRUE if the field exists on the system, otherwise FALSE.

### ACX requirements

**Minimum ACX version:** 1.1

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also
