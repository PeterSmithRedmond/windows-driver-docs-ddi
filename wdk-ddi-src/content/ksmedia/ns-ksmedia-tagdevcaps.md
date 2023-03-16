---
UID: NS:ksmedia.tagDEVCAPS
title: DEVCAPS (ksmedia.h)
description: The DEVCAPS structure describes the capabilities of an external device.
tech.root: stream
ms.date: 03/15/2023
keywords: ["tagDEVCAPS structure"]
ms.keywords: "*PDEVCAPS, DEVCAPS, DEVCAPS structure [Streaming Media Devices], PDEVCAPS, PDEVCAPS structure pointer [Streaming Media Devices], ksmedia/DEVCAPS, ksmedia/PDEVCAPS, stream.devcaps, tagDEVCAPS, vidcapstruct_61cce92e-4f74-48ff-ae84-72579136a64f.xml"
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
req.typenames: DEVCAPS, *PDEVCAPS
f1_keywords:
 - tagDEVCAPS
 - ksmedia/tagDEVCAPS
 - PDEVCAPS
 - ksmedia/PDEVCAPS
 - DEVCAPS
 - ksmedia/DEVCAPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - tagDEVCAPS
 - PDEVCAPS
 - DEVCAPS
---

## -description

The **DEVCAPS** structure describes the capabilities of an external device.

## -struct-fields

### -field CanRecord

Specifies if the external device can record.

### -field CanRecordStrobe

For multitrack devices. Specifies if the external device can record. Switches currently recording tracks off and selected nonrecording track into record.

### -field HasAudio

Specifies if the external device has audio capabilities.

### -field HasVideo

Specifies if the external device has video capabilities.

### -field UsesFiles

Specifies if the external device uses files.

### -field CanSave

Specifies if the external device can save.

### -field DeviceType

Specifies the type of the external device. See Remarks.

| Flag | Meaning |
|---|---|
| ED_DEVTYPE_VCR | Video cassette recorder |
| ED_DEVTYPE_LASERDISC | Laserdisc player |
| ED_DEVTYPE_KEYBOARD | Keyboard |
| ED_DEVTYPE_CAMERA | Video camera |
| ED_DEVTYPE_VTR | Video tape recorder |
| ED_DEVTYPE_UNKNOWN | Unknown type |

### -field TCRead

Specifies if the external device can read timecodes.

### -field TCWrite

Specifies if the external device can write timecodes.

### -field CTLRead

Specifies if the external device can read to a control track (nontimecode) target value.

### -field IndexRead

Specifies if the external device can read to an index (nontimecode) target value.

### -field Preroll

Specifies the external device's preroll time in the current time format.

### -field Postroll

Specifies the external device's postroll time in the current time format.

### -field SyncAcc

Indicates the external device's synchronization accuracy.

### -field NormRate

Specifies the external device's normal frame rate.

### -field CanPreview

Specifies if the external device can preview.

### -field CanMonitorSrc

Specifies if the external device can monitor source.

### -field CanTest

Indicates the implementation of the external device allows testing of methods/parameters by setting the high bit of a parameter that makes sense. This is not implemented an always returns FALSE.

### -field VideoIn

Indicates the external device accepts video as an input.

### -field AudioIn

Indicates the external device accepts audio as an input.

### -field Calibrate

Indicates if the external device requires calibrating.

### -field SeekType

Specifies the type of seeking the external device is capable of. For example:

| Flag | Meaning |
|---|---|
| ED_SEEK_PERFECT | Indicates device can seek to within 1 video frame without a signal break (like a DDR). |
| ED_SEEK_FAST | Indicates device can seek quick with a short break in signal. |
| ED_SEEK_SLOW | Indicates slow seeking (like a tape transport). |

### -field SimulatedHardware

Must be set to zero.

## -remarks

Any ED_Xxx tokens are defined in *xprtdefs.h* in the Microsoft DirectX SDK.

All members of the DEVCAPS structure are **TRUE** or **FALSE** unless otherwise specified.

The **DeviceType** member can be used by an application to detect the device type or its current operating mode. For example, it can return either ED_DEVTYPE_CAMERA or ED_DEVTYPE_VTR depending on a DV camcorder's mode of operation. Also, some DV devices may not be known and a device type of ED_DEVTYPE_UNKNOWN can be returned by the driver. This happens with some DV media converters.

## -see-also

[KSPROPERTY_EXTDEVICE_S](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksproperty_extdevice_s)

[TIMECODE](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-_timecode)
