---
UID: NF:scsi.FIELD_OFFSET
title: FIELD_OFFSET macro (scsi.h)
description: The FIELD_OFFSET macro (scsi.h) returns the byte offset of the specified field in the specified known structure type.
old-location: kernel\field_offset.htm
tech.root: kernel
ms.date: 02/24/2018
keywords: ["FIELD_OFFSET macro"]
ms.keywords: FIELD_OFFSET, FIELD_OFFSET function [Kernel-Mode Driver Architecture], k106_d6f0b450-e99c-4dd7-94c5-f428e4b1d642.xml, kernel.field_offset, ntdef/FIELD_OFFSET
req.header: scsi.h
req.include-header: Wdm.h, Ntddk.h, Miniport.h, Minitape.h, Scsi.h, Storport.h
req.target-type: Desktop
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.lib: scsi.h
req.dll: 
req.irql: Any level
targetos: Windows
req.typenames: SES_DOWNLOAD_MICROCODE_STATE, *PSES_DOWNLOAD_MICROCODE_STATE
f1_keywords:
 - FIELD_OFFSET
 - scsi/FIELD_OFFSET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntdef.h
api_name:
 - FIELD_OFFSET
---

# FIELD_OFFSET macro (scsi.h)


## -description

The <b>FIELD_OFFSET</b> macro returns the byte offset of a named field in a known structure type.

## -parameters

### -param type

<p>Specifies the name of a known structure type containing <i>Field</i>. </p>

### -param field

<p>Specifies the name of a field in a structure of type <i>Type</i>. </p>

## -syntax

```cpp
LONG FIELD_OFFSET(
  _In_ TYPE  Type,
  _In_ PCHAR Field
);
```

## -remarks

Used by device driver writers to symbolically determine the offset of a known field in a known structure type.

## -see-also

[**CONTAINING_RECORD**](/windows/win32/api/ntdef/nf-ntdef-containing_record)
