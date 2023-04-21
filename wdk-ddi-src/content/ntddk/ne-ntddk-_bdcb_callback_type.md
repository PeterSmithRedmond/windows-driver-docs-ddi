---
UID: NE:ntddk._BDCB_CALLBACK_TYPE
title: _BDCB_CALLBACK_TYPE (ntddk.h)
description: The BDCB_CALLBACK_TYPE enumeration specifies whether the callback being passed to a BOOT_DRIVER_CALLBACK_FUNCTION routine is a status update or a boot-start driver initialization notification.
tech.root: kernel
ms.date: 04/17/2023
keywords: ["BDCB_CALLBACK_TYPE enumeration"]
ms.keywords: "*PBDCB_CALLBACK_TYPE, BDCB_CALLBACK_TYPE, BDCB_CALLBACK_TYPE enumeration [Kernel-Mode Driver Architecture], BdCbInitializeImage, BdCbStatusUpdate, _BDCB_CALLBACK_TYPE, kernel.bdcb_callback_type, ntddk/BDCB_CALLBACK_TYPE, ntddk/BdCbInitializeImage, ntddk/BdCbStatusUpdate"
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with  Windows 8.
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
req.typenames: BDCB_CALLBACK_TYPE, *PBDCB_CALLBACK_TYPE
f1_keywords:
 - _BDCB_CALLBACK_TYPE
 - ntddk/_BDCB_CALLBACK_TYPE
 - PBDCB_CALLBACK_TYPE
 - ntddk/PBDCB_CALLBACK_TYPE
 - BDCB_CALLBACK_TYPE
 - ntddk/BDCB_CALLBACK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddk.h
api_name:
 - _BDCB_CALLBACK_TYPE
 - PBDCB_CALLBACK_TYPE
 - BDCB_CALLBACK_TYPE
---

## -description

The BDCB_CALLBACK_TYPE enumeration specifies  whether the callback being passed to a [BOOT_DRIVER_CALLBACK_FUNCTION](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback) routine is a status update or a boot-start driver initialization notification.

## -enum-fields

### -field BdCbStatusUpdate

A status update provided by the system to a boot-start driver.

### -field BdCbInitializeImage

A boot image is about to be initialized. During this callback, boot-start drivers may classify a boot image as a known good image or a known bad image.

## -remarks

The two callback types have unique context structures that provide additional information specific to the callback.

| Value | Corresponding structure to use |
|--|--|
| BdCbStatusUpdate | [**BDCB_STATUS_UPDATE_TYPE**](/windows-hardware/drivers/ddi/ntddk/ne-ntddk-_bdcb_status_update_type) |
| BdCbInitializeImage | [**BDCB_CLASSIFICATION**](/windows-hardware/drivers/ddi/ntddk/ne-ntddk-_bdcb_classification) |

## -see-also

[**BDCB_CLASSIFICATION**](/windows-hardware/drivers/ddi/ntddk/ne-ntddk-_bdcb_classification)

[**BDCB_STATUS_UPDATE_TYPE**](/windows-hardware/drivers/ddi/ntddk/ne-ntddk-_bdcb_status_update_type)

[BOOT_DRIVER_CALLBACK_FUNCTION](nc-ntddk-boot_driver_callback_function.md)
