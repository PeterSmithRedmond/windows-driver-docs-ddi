---
UID: NS:wdm._LUID_AND_ATTRIBUTES
title: LUID_AND_ATTRIBUTES (wdm.h)
description: LUID_AND_ATTRIBUTES represents a locally unique identifier (LUID) and its attributes.
tech.root: ifsk
ms.date: 12/16/2022
keywords: ["LUID_AND_ATTRIBUTES structure"]
ms.keywords: "*PLUID_AND_ATTRIBUTES, LUID_AND_ATTRIBUTES, LUID_AND_ATTRIBUTES structure [Installable File System Drivers], PLUID_AND_ATTRIBUTES, PLUID_AND_ATTRIBUTES structure pointer [Installable File System Drivers], _LUID_AND_ATTRIBUTES, ifsk.luid_and_attributes, securitystructures_372f1a20-6582-4904-8de1-8efd9950ab76.xml, wdm/LUID_AND_ATTRIBUTES, wdm/PLUID_AND_ATTRIBUTES"
req.header: wdm.h
req.include-header: Ntddk.h, Ntifs.h, Fltkernel.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LUID_AND_ATTRIBUTES, *PLUID_AND_ATTRIBUTES
f1_keywords:
 - _LUID_AND_ATTRIBUTES
 - wdm/_LUID_AND_ATTRIBUTES
 - PLUID_AND_ATTRIBUTES
 - wdm/PLUID_AND_ATTRIBUTES
 - LUID_AND_ATTRIBUTES
 - wdm/LUID_AND_ATTRIBUTES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - _LUID_AND_ATTRIBUTES
 - PLUID_AND_ATTRIBUTES
 - LUID_AND_ATTRIBUTES
---

## -description

**LUID_AND_ATTRIBUTES** represents a locally unique identifier (LUID) and its attributes.

## -struct-fields

### -field Luid

An LUID value.

### -field Attributes

Specifies attributes of the LUID. This value contains up to 32 one-bit flags. Its meaning depends on the definition and use of the LUID.

The following attributes are defined for privileges:

| Attribute | Description |
|---|---|
| SE_PRIVILEGE_ENABLED | The privilege is enabled. |
| SE_PRIVILEGE_ENABLED_BY_DEFAULT | The privilege is enabled by default. |
| SE_PRIVILEGE_USED_FOR_ACCESS | The privilege was used to gain access to an object or service. This flag is used to identify the relevant privileges in a set passed by a client application that may contain unnecessary privileges. |

## -remarks

An LUID_AND_ATTRIBUTES structure can represent an LUID whose attributes change frequently, such as when it is used to represent privileges in the PRIVILEGE_SET structure. Privileges are represented by LUIDs and have attributes indicating whether they are currently enabled or disabled.

Be aware of the following derived types:

```cpp
typedef LUID_AND_ATTRIBUTES LUID_AND_ATTRIBUTES_ARRAY[ANYSIZE_ARRAY];
typedef LUID_AND_ATTRIBUTES_ARRAY *PLUID_AND_ATTRIBUTES_ARRAY;
```

## -see-also

[**LUID**](../igpupvdev/ns-igpupvdev-_luid.md)

[**PRIVILEGE_SET**](/previous-versions/windows/hardware/drivers/ff551860(v=vs.85))

[SeFilterToken](../ntifs/nf-ntifs-sefiltertoken.md)

[SePrivilegeCheck](../ntifs/nf-ntifs-seprivilegecheck.md)