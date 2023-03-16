---
UID: NS:ksmedia.tagKS_MPEAUDIOINFO
title: tagKS_MPEAUDIOINFO (ksmedia.h)
description: The KS_MPEGAUDIOINFO structure describes an MPEG audio stream.
tech.root: stream
ms.date: 03/15/2023
keywords: ["tagKS_MPEAUDIOINFO structure"]
ms.keywords: "*PKS_MPEGAUDIOINFO, KS_MPEGAUDIOINFO, KS_MPEGAUDIOINFO structure [Streaming Media Devices], PKS_MPEGAUDIOINFO, PKS_MPEGAUDIOINFO structure pointer [Streaming Media Devices], ksmedia/KS_MPEGAUDIOINFO, ksmedia/PKS_MPEGAUDIOINFO, stream.ks_mpegaudioinfo, tagKS_MPEAUDIOINFO, vidcapstruct_613d53ce-69cd-46da-9bd8-0ac41ca12129.xml"
req.header: ksmedia.h
req.include-header: Ksmedia.h
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
req.typenames: KS_MPEGAUDIOINFO, *PKS_MPEGAUDIOINFO
f1_keywords:
 - tagKS_MPEAUDIOINFO
 - ksmedia/tagKS_MPEAUDIOINFO
 - PKS_MPEGAUDIOINFO
 - ksmedia/PKS_MPEGAUDIOINFO
 - KS_MPEGAUDIOINFO
 - ksmedia/KS_MPEGAUDIOINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - tagKS_MPEAUDIOINFO
 - PKS_MPEGAUDIOINFO
 - KS_MPEGAUDIOINFO
---

## -description

The **KS_MPEGAUDIOINFO** structure describes an MPEG audio stream.

## -struct-fields

### -field dwFlags

Specifies the time base for audio timestamps. Reject the connection if undefined bits are not 0. The following flag is defined.

| Flag | Meaning |
|---|---|
| KS_MPEGAUDIOINFO_27MhzTimebase | Specifies that PTS and DTS timestamps advance at 27 MHz rather than 90 kHz. |

### -field dwReserved1

Must be 0; otherwise, reject the connection.

### -field dwReserved2

Must be 0; otherwise, reject the connection.

### -field dwReserved3

Must be 0; otherwise, reject the connection.
