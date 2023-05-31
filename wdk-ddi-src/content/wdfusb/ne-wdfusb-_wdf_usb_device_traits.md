---
UID: NE:wdfusb._WDF_USB_DEVICE_TRAITS
title: _WDF_USB_DEVICE_TRAITS (wdfusb.h)
description: The WDF_USB_DEVICE_TRAITS enumeration identifies USB device traits.
old-location: wdf\wdf_usb_device_traits.htm
tech.root: wdf
ms.date: 02/26/2018
keywords: ["WDF_USB_DEVICE_TRAITS enumeration"]
ms.keywords: DFUsbRef_504c0bd9-3ba7-47cc-a99d-ab54d46cbdc4.xml, WDF_USB_DEVICE_TRAITS, WDF_USB_DEVICE_TRAITS enumeration, WDF_USB_DEVICE_TRAIT_AT_HIGH_SPEED, WDF_USB_DEVICE_TRAIT_REMOTE_WAKE_CAPABLE, WDF_USB_DEVICE_TRAIT_SELF_POWERED, _WDF_USB_DEVICE_TRAITS, kmdf.wdf_usb_device_traits, wdf.wdf_usb_device_traits, wdfusb/WDF_USB_DEVICE_TRAITS, wdfusb/WDF_USB_DEVICE_TRAIT_AT_HIGH_SPEED, wdfusb/WDF_USB_DEVICE_TRAIT_REMOTE_WAKE_CAPABLE, wdfusb/WDF_USB_DEVICE_TRAIT_SELF_POWERED
req.header: wdfusb.h
req.include-header: Wdfusb.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
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
req.typenames: WDF_USB_DEVICE_TRAITS
f1_keywords:
 - _WDF_USB_DEVICE_TRAITS
 - wdfusb/_WDF_USB_DEVICE_TRAITS
 - WDF_USB_DEVICE_TRAITS
 - wdfusb/WDF_USB_DEVICE_TRAITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdfusb.h
api_name:
 - _WDF_USB_DEVICE_TRAITS
 - WDF_USB_DEVICE_TRAITS
---

# _WDF_USB_DEVICE_TRAITS enumeration


## -description

<p class="CCE_Message">[Applies to KMDF and UMDF]</p>

The <b>WDF_USB_DEVICE_TRAITS</b> enumeration identifies USB device traits.

## -enum-fields

### -field WDF_USB_DEVICE_TRAIT_SELF_POWERED:0x00000001

The device is self-powered.

### -field WDF_USB_DEVICE_TRAIT_REMOTE_WAKE_CAPABLE:0x00000002

The device has a remote wakeup capability.

### -field WDF_USB_DEVICE_TRAIT_AT_HIGH_SPEED:0x00000004

The device is operating at high speed or SuperSpeed.

## -remarks

The <b>WDF_USB_DEVICE_TRAITS</b> enumeration is used in the <a href="/windows-hardware/drivers/ddi/wdfusb/ns-wdfusb-_wdf_usb_device_information">WDF_USB_DEVICE_INFORMATION</a> structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdfusb/ns-wdfusb-_wdf_usb_device_information">WDF_USB_DEVICE_INFORMATION</a>

