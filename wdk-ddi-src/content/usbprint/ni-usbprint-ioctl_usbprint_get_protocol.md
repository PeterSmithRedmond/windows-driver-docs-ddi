---
UID: NI:usbprint.IOCTL_USBPRINT_GET_PROTOCOL
title: IOCTL_USBPRINT_GET_PROTOCOL
description: Retrieve the current printer protocol code of the USB printer interface.
tech.root: print
ms.date: 04/19/2022
keywords: ["IOCTL_USBPRINT_GET_PROTOCOL IOCTL"]
req.header: usbprint.h
req.include-header: Usbprint.h
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
f1_keywords:
 - IOCTL_USBPRINT_GET_PROTOCOL
 - usbprint/IOCTL_USBPRINT_GET_PROTOCOL
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - usbprint.h
api_name:
 - IOCTL_USBPRINT_GET_PROTOCOL
product:
 - Windows
---

### Major Code:  [IRP_MJ_DEVICE_CONTROL](/windows-hardware/drivers/kernel/irp-mj-device-control)

## -description

Retrieve the current printer protocol code of the USB printer interface.

## -ioctlparameters

### -ioctl-major-code

### -input-buffer

NULL

### -input-buffer-length

0

### -output-buffer

Pointer to a DWORD

### -output-buffer-length

sizeof(DWORD)

### -in-out-buffer

### -inout-buffer-length

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.
Otherwise, Status to the appropriate error condition as a NTSTATUS code.

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/using-ntstatus-values).

## -remarks

IOCTL_USBPRINT_GET_PROTOCOL returns one of the following values:

| Defined constant | Value |
|--|--|
| USB_PRINTER_PROTOCOL_BIDI | 2 |
| USB_PRINTER_PROTOCOL_IPPOVERUSB | 4 |

## -see-also
