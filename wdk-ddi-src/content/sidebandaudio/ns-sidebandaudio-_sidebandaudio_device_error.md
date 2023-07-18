---
UID: NS:sidebandaudio._SIDEBANDAUDIO_DEVICE_ERROR
title: _SIDEBANDAUDIO_DEVICE_ERROR (sidebandaudio.h)
description: The SIDEBANDAUDIO_DEVICE_ERROR structure describes the error reported on the Device.
ms.date: 07/11/2023
keywords: ["SIDEBANDAUDIO_DEVICE_ERROR structure"]
ms.keywords: _SIDEBANDAUDIO_DEVICE_ERROR, SIDEBANDAUDIO_DEVICE_ERROR, *PSIDEBANDAUDIO_DEVICE_ERROR,
req.header: sidebandaudio.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: SIDEBANDAUDIO_DEVICE_ERROR, *PSIDEBANDAUDIO_DEVICE_ERROR
targetos: Windows
tech.root: audio
ms.custom: RS5
f1_keywords:
 - _SIDEBANDAUDIO_DEVICE_ERROR
 - sidebandaudio/_SIDEBANDAUDIO_DEVICE_ERROR
 - PSIDEBANDAUDIO_DEVICE_ERROR
 - sidebandaudio/PSIDEBANDAUDIO_DEVICE_ERROR
 - SIDEBANDAUDIO_DEVICE_ERROR
 - sidebandaudio/SIDEBANDAUDIO_DEVICE_ERROR
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sidebandaudio.h
api_name:
 - _SIDEBANDAUDIO_DEVICE_ERROR
 - PSIDEBANDAUDIO_DEVICE_ERROR
 - SIDEBANDAUDIO_DEVICE_ERROR
---

# SIDEBANDAUDIO_DEVICE_ERROR structure

## -description

The **SIDEBANDAUDIO_DEVICE_ERROR** structure describes the error reported on the Device.

## -struct-fields

### -field EpIndex

Zero based index indicating the Endpoint on device.

### -field Immediate

Indicates whether IOCTL current value is requested or IRP should complete upon next change in value.

### -field Status

Indicates status of the device.

## -remarks

## -requirements

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | sidebandaudio.h |

## -see-also

[sidebandaudio.h](index.md)
