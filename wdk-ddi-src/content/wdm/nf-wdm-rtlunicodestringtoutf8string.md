---
UID: NF:wdm.RtlUnicodeStringToUTF8String
title: RtlUnicodeStringToUTF8String function (wdm.h)
description: The RtlUnicodeStringToUTF8String function converts the specified Unicode source string into an UTF8 string.
tech.root: kernel
ms.date: 05/27/2021
ms.keywords: RtlUnicodeStringToUTF8String
req.header: wdm.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wdm.h
api_name:
 - RtlUnicodeStringToUTF8String
f1_keywords:
 - RtlUnicodeStringToUTF8String
 - wdm/RtlUnicodeStringToUTF8String
---

# RtlUnicodeStringToUTF8String function (wdm.h)

## -description

The **RtlUnicodeStringToUTF8String** function converts the specified Unicode source string into an UTF8 string.

## -parameters

### -param DestinationString

Pointer to a [**UTF8_STRING**](/windows/win32/api/ntdef/ns-ntdef-string) structure to hold the converted UTF8 string.  If *AllocateDestinationString* is **TRUE**, the routine allocates a new buffer to hold the string data, and updates the **Buffer** member of *DestinationString* to point to the new buffer. Otherwise, the routine uses the currently specified buffer to hold the string.  The maximum length field is only set if *AllocateDestinationString* is TRUE.

### -param SourceString

Pointer to the Unicode source string to be converted to UTF8.

### -param AllocateDestinationString

**TRUE** if this routine is to allocate the buffer space for the *DestinationString*. If it does, the buffer must be deallocated by calling [**RtlFreeUTF8String**](./nf-wdm-rtlfreeutf8string.md).

## -returns

If the conversion succeeds, **RtlUnicodeStringToUTF8String** returns STATUS_SUCCESS. On failure, the routine does not allocate memory or perform a conversion.

## -see-also

[**RtlFreeUTF8String**](./nf-wdm-rtlfreeutf8string.md)
