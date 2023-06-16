---
UID: NI:kbdmou.IOCTL_INTERNAL_KEYBOARD_DISCONNECT
title: IOCTL_INTERNAL_KEYBOARD_DISCONNECT (kbdmou.h)
description: The IOCTL_INTERNAL_KEYBOARD_DISCONNECT request is completed with a status of STATUS_NOT_IMPLEMENTED. Note that a Plug and Play keyboard can be added or removed by the Plug and Play manager.
old-location: hid\ioctl_internal_keyboard_disconnect.htm
tech.root: hid
ms.date: 04/30/2018
keywords: ["IOCTL_INTERNAL_KEYBOARD_DISCONNECT IOCTL"]
ms.keywords: IOCTL_INTERNAL_KEYBOARD_DISCONNECT, IOCTL_INTERNAL_KEYBOARD_DISCONNECT control, IOCTL_INTERNAL_KEYBOARD_DISCONNECT control code [Human Input Devices], hid.ioctl_internal_keyboard_disconnect, kbdmou/IOCTL_INTERNAL_KEYBOARD_DISCONNECT, kfilref_fd52cb0d-fbdd-44fb-9c71-ec829387a88b.xml
req.header: kbdmou.h
req.include-header: Kbdmou.h
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
 - IOCTL_INTERNAL_KEYBOARD_DISCONNECT
 - kbdmou/IOCTL_INTERNAL_KEYBOARD_DISCONNECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - kbdmou.h
api_name:
 - IOCTL_INTERNAL_KEYBOARD_DISCONNECT
---

# IOCTL_INTERNAL_KEYBOARD_DISCONNECT IOCTL


## -description

The IOCTL_INTERNAL_KEYBOARD_DISCONNECT request is completed with a status of STATUS_NOT_IMPLEMENTED. Note that a Plug and Play keyboard can be added or removed by the Plug and Play manager.

## -ioctlparameters

### -ioctl-major-code

[IRP_MJ_INTERNAL_DEVICE_CONTROL](/windows-hardware/drivers/kernel/irp-mj-internal-device-control)

### -input-buffer

None

### -input-buffer-length

None

### -output-buffer

None

### -output-buffer-length

None

### -in-out-buffer

### -inout-buffer-length

### -status-block

The <b>Status</b> member is set to STATUS_NOT_IMPLEMENTED.

## -see-also

<a href="/windows-hardware/drivers/ddi/kbdmou/ni-kbdmou-ioctl_internal_keyboard_connect">IOCTL_INTERNAL_KEYBOARD_CONNECT</a>
