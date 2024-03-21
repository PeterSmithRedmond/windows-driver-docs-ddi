---
UID: NF:wdm.RtlFreeUTF8String
title: RtlFreeUTF8String function
description: The RtlFreeUTF8String function releases storage that was allocated by RtlUnicodeStringToUTF8String.
tech.root: kernel
ms.date: 03/24/2020
ms.keywords: RtlFreeUTF8String
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
 - RtlFreeUTF8String
f1_keywords:
 - RtlFreeUTF8String
 - wdm/RtlFreeUTF8String
---

# RtlFreeUTF8String function

## -description

The **RtlFreeUTF8String** function releases storage that was allocated by [**RtlUnicodeStringToUTF8String**](./nf-wdm-rtlunicodestringtoutf8string.md).

## -parameters

### -param utf8String

Pointer to the UTF8 string buffer previously allocated by **RtlUnicodeStringToUTF8String**.

## -returns

## -remarks

This routine only releases the UTF8 string buffer passed to it; it does not release the Unicode string buffer passed to **RtlUnicodeStringToUTF8String**.

## -see-also

[**RtlUnicodeStringToUTF8String**](./nf-wdm-rtlunicodestringtoutf8string.md)
