---
UID: NF:wiamdef.wiasValidateItemProperties
title: wiasValidateItemProperties function (wiamdef.h)
description: The wiasValidateItemProperties function validates a list of simple item properties against their current valid values.
tech.root: image
ms.date: 03/08/2023
keywords: ["wiasValidateItemProperties function"]
ms.keywords: image.wiasvalidateitemproperties, wiamdef/wiasValidateItemProperties, wiasFncs_98dc1f86-1cba-43c0-9f2a-3598701439bc.xml, wiasValidateItemProperties, wiasValidateItemProperties function [Imaging Devices]
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - wiasValidateItemProperties
 - wiamdef/wiasValidateItemProperties
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wiaservc.dll
api_name:
 - wiasValidateItemProperties
---

## -description

The **wiasValidateItemProperties** function validates a list of simple item properties against their current valid values.

## -parameters

### -param pWiasContext [in]

Pointer to a WIA item context.

### -param nPropSpec

Specifies the number of properties to validate.

### -param pPropSpec [in]

Pointer to the first element of an array of PROPSPEC structures indicating the properties to validate.

## -returns

On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).

## -remarks

This function validates simple property values of the following types grouped by attribute.

| Attributes | Supported Types |
|---|---|
| WIA_PROP_FLAG | VT_UI1, VT_UI2, VT_UI4, VT_UI8, VT_I1, VT_I2, VT_I4 |
| WIA_PROP_RANGE | VT_UI1, VT_UI2, VT_UI4, VT_UI8, VT_I1, VT_I2, VT_I4, VT_R4, VT_R8 |
| WIA_PROP_LIST | VT_UI1, VT_UI2, VT_UI4, VT_UI8, VT_I1, VT_I2, VT_I4, VT_R4, VT_R8, VT_BSTR |

The PROPSPEC structure is defined in the Windows SDK documentation.
