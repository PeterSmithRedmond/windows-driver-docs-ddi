---
UID: NI:usbfnioctl.IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS
title: IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS (usbfnioctl.h)
description: Do not use.
old-location: buses\ioctl_internal_usbfn_deactivate_usb_bus.htm
tech.root: usbref
ms.date: 05/07/2018
keywords: ["IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS IOCTL"]
ms.keywords: IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS, IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS control, IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS control code [Buses], buses.ioctl_internal_usbfn_deactivate_usb_bus, usbfnioctl/IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS
req.header: usbfnioctl.h
req.include-header: Usbfnioctl.h
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
req.typenames: 
f1_keywords:
 - IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS
 - usbfnioctl/IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbfnioctl.h
api_name:
 - IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS
---

# IOCTL_INTERNAL_USBFN_DEACTIVATE_USB_BUS IOCTL


## -description

Do not use.

## -ioctlparameters

### -ioctl-major-code

[IRP_MJ_INTERNAL_DEVICE_CONTROL](/windows-hardware/drivers/kernel/irp-mj-internal-device-control)

### -input-buffer

NULL.

### -input-buffer-length

None.

### -output-buffer

NULL.

### -output-buffer-length

None.

### -in-out-buffer

### -inout-buffer-length

### -status-block

If the request is successful, the USB function class extension (UFX) returns STATUS_SUCCESS, or another status value for which NT_SUCCESS(status) equals TRUE. Otherwise it returns a status value for which NT_SUCCESS(status) equals FALSE.

