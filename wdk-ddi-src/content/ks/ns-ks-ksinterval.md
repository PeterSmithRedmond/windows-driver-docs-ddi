---
UID: NS:ks.KSINTERVAL
title: KSINTERVAL (ks.h)
description: The KSINTERVAL structure specifies a base time and time interval for recurring events.
old-location: stream\ksinterval.htm
tech.root: stream
ms.date: 04/23/2018
keywords: ["KSINTERVAL structure"]
ms.keywords: "*PKSINTERVAL, KSINTERVAL, KSINTERVAL structure [Streaming Media Devices], PKSINTERVAL, PKSINTERVAL structure pointer [Streaming Media Devices], ks-struct_56fded71-9af4-46a7-b872-1660582179ad.xml, ks/KSINTERVAL, ks/PKSINTERVAL, stream.ksinterval"
req.header: ks.h
req.include-header: Ks.h
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
req.typenames: KSINTERVAL, *PKSINTERVAL
f1_keywords:
 - PKSINTERVAL
 - ks/PKSINTERVAL
 - KSINTERVAL
 - ks/KSINTERVAL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ks.h
api_name:
 - PKSINTERVAL
 - KSINTERVAL
---

# KSINTERVAL structure


## -description

The KSINTERVAL structure specifies a base time and time interval for recurring events.

## -struct-fields

### -field TimeBase

Specifies a 64-bit time base.

### -field Interval

Specifies a recurrence interval, also 64-bit.

## -see-also

<a href="/windows-hardware/drivers/stream/ksevent-clock-interval-mark">KSEVENT_CLOCK_INTERVAL_MARK</a>



<a href="/windows-hardware/drivers/stream/ksevent-clock-position-mark">KSEVENT_CLOCK_POSITION_MARK</a>

