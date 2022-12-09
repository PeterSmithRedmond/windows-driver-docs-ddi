---
UID: NS:ntddk._WHEA_TIMESTAMP
title: WHEA_TIMESTAMP (ntddk.h)
description: The WHEA_TIMESTAMP union describes the time that an error was reported to the operating system.
tech.root: whea
ms.date: 12/09/2022
keywords: ["WHEA_TIMESTAMP structure"]
ms.keywords: "*PWHEA_TIMESTAMP, PWHEA_TIMESTAMP, PWHEA_TIMESTAMP union pointer [WHEA Drivers and Applications], WHEA_TIMESTAMP, WHEA_TIMESTAMP union [WHEA Drivers and Applications], _WHEA_TIMESTAMP, ntddk/PWHEA_TIMESTAMP, ntddk/WHEA_TIMESTAMP, whea.whea_timestamp, whearef_d0fafe3b-0cea-4adf-a68a-b565e04ae258.xml"
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: Supported in Windows Server 2008, Windows Vista SP1, and later versions of Windows.
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
req.typenames: WHEA_TIMESTAMP, *PWHEA_TIMESTAMP
f1_keywords:
 - _WHEA_TIMESTAMP
 - ntddk/_WHEA_TIMESTAMP
 - PWHEA_TIMESTAMP
 - ntddk/PWHEA_TIMESTAMP
 - WHEA_TIMESTAMP
 - ntddk/WHEA_TIMESTAMP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddk.h
api_name:
 - _WHEA_TIMESTAMP
 - PWHEA_TIMESTAMP
 - WHEA_TIMESTAMP
---

## -description

The **WHEA_TIMESTAMP** union describes the time that an error was reported to the operating system.

## -struct-fields

### -field DUMMYSTRUCTNAME

Defines the **DUMMYSTRUCTNAME** structure.

### -field DUMMYSTRUCTNAME.Seconds

The number of seconds past the minute.

### -field DUMMYSTRUCTNAME.Minutes

The number of minutes past the hour.

### -field DUMMYSTRUCTNAME.Hours

The hour in the day.

### -field DUMMYSTRUCTNAME.Precise

If this member is set to 1, the timestamp correlates precisely to the time of the error event.

This member is supported in Windows 7 and later versions of Windows.

### -field DUMMYSTRUCTNAME.Reserved

Reserved for system use.

### -field DUMMYSTRUCTNAME.Day

The day of the month.

### -field DUMMYSTRUCTNAME.Month

The month of the year.

### -field DUMMYSTRUCTNAME.Year

The year within the century.

### -field DUMMYSTRUCTNAME.Century

The century.

### -field AsLARGE_INTEGER

A LARGE_INTEGER representation of the contents of the **WHEA_TIMESTAMP** union.

## -remarks

A **WHEA_TIMESTAMP** union is contained within the [WHEA_ERROR_RECORD_HEADER](/windows-hardware/drivers/ddi/ntddk/ns-ntddk-_whea_error_record_header) structure.

## -see-also

[WHEA_ERROR_RECORD_HEADER](/windows-hardware/drivers/ddi/ntddk/ns-ntddk-_whea_error_record_header)
