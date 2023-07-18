---
UID: NI:sidebandaudio.IOCTL_SBAUD_GET_SUPPORTED_FORMATS
title: IOCTL_SBAUD_GET_SUPPORTED_FORMATS (sidebandaudio.h)
description: "The audio driver issues the IOCTL_SBAUD_GET_SUPPORTED_FORMATS control code to get information about the stream formats supported by sideband audio endpoint."
ms.date: 07/14/2023
keywords: ["IOCTL_SBAUD_GET_SUPPORTED_FORMATS IOCTL"]
req.header: sidebandaudio.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.max-support: 
targetos: Windows
tech.root: audio
ms.custom: RS5
f1_keywords:
 - IOCTL_SBAUD_GET_SUPPORTED_FORMATS
 - sidebandaudio/IOCTL_SBAUD_GET_SUPPORTED_FORMATS
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sidebandaudio.h
api_name:
 - IOCTL_SBAUD_GET_SUPPORTED_FORMATS
---

# IOCTL_SBAUD_GET_SUPPORTED_FORMATS IOCTL

## -description

The audio driver issues the **IOCTL_SBAUD_GET_SUPPORTED_FORMATS** control code to get information about the stream formats supported by sideband audio endpoint.

## -ioctlparameters

### -ioctl-major-code

[IRP_MJ_DEVICE_CONTROL](/windows-hardware/drivers/kernel/irp-mj-device-control)

### -input-buffer

[SIDEBANDAUDIO_SUPPORTED_FORMATS](./ns-sidebandaudio-_sidebandaudio_supported_formats.md) containing endpoint index, and array of formats supported by the Audio driver.

### -input-buffer-length

Size of [SIDEBANDAUDIO_SUPPORTED_FORMATS](./ns-sidebandaudio-_sidebandaudio_supported_formats.md) including storage for array of formats.

### -output-buffer

[SIDEBANDAUDIO_SUPPORTED_FORMATS](./ns-sidebandaudio-_sidebandaudio_supported_formats.md). The sideband driver will return the intersection of the sideband audio formats with the formats supplied by the audio driver as an input parameter.

### -output-buffer-length

Size of [SIDEBANDAUDIO_SUPPORTED_FORMATS](./ns-sidebandaudio-_sidebandaudio_supported_formats.md) including storage for array of formats.

### -in-out-buffer

### -inout-buffer-length

### -status-block

If the routine succeeds, then Status is set to STATUS_SUCCESS and the <i>Information</i> member is the number of bytes that the routine writes to the output buffer.

If Status is set to STATUS_BUFFER_TOO_SMALL, then the audio driver should read the <i>Information</i> member to get the size of the buffer that the caller should allocate for this request.

## -remarks

## -requirements

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | sidebandaudio.h |

## -see-also

[SIDEBANDAUDIO_SUPPORTED_FORMATS](./ns-sidebandaudio-_sidebandaudio_supported_formats.md)

[Introduction to I/O Control Codes](/windows-hardware/drivers/kernel/introduction-to-i-o-control-codes)

[sidebandaudio.h](index.md)