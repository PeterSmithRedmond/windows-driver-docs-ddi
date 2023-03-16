---
UID: NS:ksmedia.KSPROPERTY_TUNER_SCAN_STATUS_S
title: KSPROPERTY_TUNER_SCAN_STATUS_S (ksmedia.h)
description: The KSPROPERTY_TUNER_SCAN_STATUS_S structure describes status for a scanning operation.
tech.root: stream
ms.date: 03/14/2023
keywords: ["KSPROPERTY_TUNER_SCAN_STATUS_S structure"]
ms.keywords: "*PKSPROPERTY_TUNER_SCAN_STATUS_S, KSPROPERTY_TUNER_SCAN_STATUS_S, KSPROPERTY_TUNER_SCAN_STATUS_S structure [Streaming Media Devices], PKSPROPERTY_TUNER_SCAN_STATUS_S, PKSPROPERTY_TUNER_SCAN_STATUS_S structure pointer [Streaming Media Devices], ksmedia/KSPROPERTY_TUNER_SCAN_STATUS_S, ksmedia/PKSPROPERTY_TUNER_SCAN_STATUS_S, stream.ksproperty_tuner_scan_status_s, vidcapstruct_70c7d301-6c91-4955-bcaa-67cad29cb15a.xml"
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the operating system.
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
req.typenames: KSPROPERTY_TUNER_SCAN_STATUS_S, *PKSPROPERTY_TUNER_SCAN_STATUS_S
f1_keywords:
 - PKSPROPERTY_TUNER_SCAN_STATUS_S
 - ksmedia/PKSPROPERTY_TUNER_SCAN_STATUS_S
 - KSPROPERTY_TUNER_SCAN_STATUS_S
 - ksmedia/KSPROPERTY_TUNER_SCAN_STATUS_S
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - PKSPROPERTY_TUNER_SCAN_STATUS_S
 - KSPROPERTY_TUNER_SCAN_STATUS_S
---

## -description

The **KSPROPERTY_TUNER_SCAN_STATUS_S** structure describes status for a scanning operation.

## -struct-fields

### -field Property

Specifies an initialized [KSPROPERTY](/windows-hardware/drivers/stream/ksproperty-structure) structure that describes the property set, property ID, and request type.

### -field LockStatus

One of the following values from the **TunerLockType** enumeration that indicates the lock status of the scanning operation.

| Status | Meaning |
|---|---|
| **Tuner_LockType_None** (0x00) | The tuner is not locked on a signal. The driver can return this value at the end of a scan. |
| **Tuner_LockType_Within_Scan_Sensing_Range** (0x01) | The signal is nearby; however, the driver cannot report the exact frequency. |
| **Tuner_LockType_Locked** (0x02) | A fine-tune signal lock was established. The driver can return this value at the end of a scan. |

### -field CurrentFrequency

The current locked-in frequency, in Hz, on the tuning device.

## -see-also

[KSEVENT_TUNER_INITIATE_SCAN](/windows-hardware/drivers/stream/ksevent-tuner-initiate-scan)

[KSPROPERTY](/windows-hardware/drivers/stream/ksproperty-structure)

[KSPROPERTY_TUNER_SCAN_STATUS](/windows-hardware/drivers/stream/ksproperty-tuner-scan-status)

[PROPSETID_TUNER](/windows-hardware/drivers/stream/propsetid-tuner)
