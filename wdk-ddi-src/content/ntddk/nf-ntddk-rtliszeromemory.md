---
UID: NF:ntddk.RtlIsZeroMemory
title: RtlIsZeroMemory function
description: This routine checks if a block of unaligned memory is all zero.
tech.root: kernel
ms.date: 06/13/2021
ms.keywords: RtlIsZeroMemory
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: 
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
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
 - HeaderDef
api_location:
 - NtosKrnl.exe
api_name:
 - RtlIsZeroMemory
f1_keywords:
 - RtlIsZeroMemory
 - ntddk/RtlIsZeroMemory
---

# RtlIsZeroMemory function

## -description

This routine checks if a block of unaligned memory is all zero.

## -parameters

### -param Buffer

Pointer to the memory buffer to check.

### -param Length

Length, in bytes, of the memory buffer.

## -returns

This function returns **TRUE** if the memory is all zero and **FALSE** otherwise.

## -remarks

## -see-also
