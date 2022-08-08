---
UID: NS:pep_x._PEP_PPM_FEEDBACK_READ
title: _PEP_PPM_FEEDBACK_READ (pep_x.h)
description: Learn how the PEP_PPM_FEEDBACK_READ structure contains the value read from a processor performance feedback counter.
old-location: kernel\pep_ppm_feedback_read.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["PEP_PPM_FEEDBACK_READ structure"]
ms.keywords: "*PPEP_PPM_FEEDBACK_READ, PEP_PPM_FEEDBACK_READ, PEP_PPM_FEEDBACK_READ structure [Kernel-Mode Driver Architecture], PPEP_PPM_FEEDBACK_READ, PPEP_PPM_FEEDBACK_READ structure pointer [Kernel-Mode Driver Architecture], _PEP_PPM_FEEDBACK_READ, kernel.pep_ppm_feedback_read, pepfx/PEP_PPM_FEEDBACK_READ, pepfx/PPEP_PPM_FEEDBACK_READ"
req.header: pep_x.h
req.include-header: Pep_x.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 10.
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
req.typenames: PEP_PPM_FEEDBACK_READ, *PPEP_PPM_FEEDBACK_READ
f1_keywords:
 - _PEP_PPM_FEEDBACK_READ
 - pep_x/_PEP_PPM_FEEDBACK_READ
 - PPEP_PPM_FEEDBACK_READ
 - pep_x/PPEP_PPM_FEEDBACK_READ
 - PEP_PPM_FEEDBACK_READ
 - pep_x/PEP_PPM_FEEDBACK_READ
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - pepfx.h
api_name:
 - _PEP_PPM_FEEDBACK_READ
 - PPEP_PPM_FEEDBACK_READ
 - PEP_PPM_FEEDBACK_READ
---

# _PEP_PPM_FEEDBACK_READ structure (pep_x.h)

## -description

The **PEP_PPM_FEEDBACK_READ** structure contains the value read from a processor performance feedback counter.

## -struct-fields

### -field CounterIndex

The index that identifies which processor performance feedback counter to read. If the platform extension plug-in (PEP) supports N counters for this processor, counter indexes range from 0 to N-1. The PEP previously supplied the number of supported counters in response to a [PEP_NOTIFY_PPM_QUERY_CAPABILITIES](../pepfx/ns-pepfx-_pep_ppm_query_capabilities.md) notification.

### -field InstantaneousValue

The current instantaneous value read from the counter, if the counter generates an instantaneous value.

### -field NominalCount

The nominal accumulated value of the counter. The accumulated value is the sum of all actual values that have so far been read from the counter hardware.

### -field ActualCount

The actual value read from the counter.

## -remarks

The unnamed union contains rither an instantaneous counter value, if the counter generates an instantaneous value, or both relative and accumulated counter values, if the counter hardware generates a relative value.

This structure is used by the [PEP_NOTIFY_PPM_FEEDBACK_READ](../pepfx/ns-pepfx-_pep_ppm_feedback_read.md) notification. The **CounterIndex** member of the structure contains an input value supplied by the Windows [power management framework](../_kernel/index.md#device-power-management) (PoFx) when this notification is set. The other members contain output values that the PEP writes to the structure in response to the notification. The PEP writes to the **InstantaneousValue** member if the counter generates an instantaneous value, or to the **NominalCount** and **ActualCount** members if the counter generates a relative value.

Both an instantaneous counter and a relative counter are reset to zero when power is first turned on, but reading a relative counter causes the count to reset to zero, whereas reading an instantaneous counter does not reset the count. The PEP previously indicated whether the counter is instantaneous or relative in response to a [PEP_NOTIFY_PPM_QUERY_FEEDBACK_COUNTERS](../pepfx/ns-pepfx-_pep_ppm_query_feedback_counters.md) notification.

## -see-also

- [PEP_NOTIFY_PPM_FEEDBACK_READ](../pepfx/ns-pepfx-_pep_ppm_feedback_read.md)
- [PEP_NOTIFY_PPM_QUERY_CAPABILITIES](../pepfx/ns-pepfx-_pep_ppm_query_capabilities.md)
- [PEP_NOTIFY_PPM_QUERY_FEEDBACK_COUNTERS](../pepfx/ns-pepfx-_pep_ppm_query_feedback_counters.md)
