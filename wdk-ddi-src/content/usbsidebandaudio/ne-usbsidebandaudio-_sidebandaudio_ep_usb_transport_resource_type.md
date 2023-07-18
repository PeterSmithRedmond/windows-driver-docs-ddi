---
UID: NE:usbsidebandaudio._SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
title: _SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE (usbsidebandaudio.h)
description: Describes the type of transport resource.
ms.date: 07/11/2023
keywords: ["SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE enumeration"]
ms.keywords: _SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE, SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE,
req.header: usbsidebandaudio.h
req.include-header: usbsidebandaudio.h
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
targetos: Windows
tech.root: audio
ms.custom: RS5
f1_keywords:
 - _SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
 - usbsidebandaudio/_SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
 - SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
 - usbsidebandaudio/SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - usbsidebandaudio.h
api_name:
 - _SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
 - SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE
---

# _SIDEBANDAUDIO_EP_USB_TRANSPORT_RESOURCE_TYPE enumeration

## -description

Describes the type of transport resource. The resources will be returned in the output buffer.

## -enum-fields

### -field SIOP_TYPE_USBAUD_USBD_INTERFACE_DESCRIPTOR

[USB Interface Descriptor](../usbspec/ns-usbspec-_usb_interface_descriptor.md)

### -field SIOP_TYPE_USBAUD_EP_USBD_ENDPOINT_DESCRIPTOR

[USBD Endpoint Descriptor](../usbspec/ns-usbspec-_usb_endpoint_descriptor.md)

### -field SIOP_TYPE_USBAUD_EP_USBD_ENDPOINT_OFFLOAD_INFORMATION

[USBD Endpoint Offload Information](../usb/ns-usb-_usbd_endpoint_offload_information.md)

### -field SIOP_TYPE_USBAUD_EP_USBAUDIO_TRANSPORT_RESOURCES

[Sideband Audio EP transport resource](./ns-usbsidebandaudio-_sidebandaudio_ep_usbaudio_transport_resources.md)

### -field SIOP_TYPE_USBAUD_EP_OFFLOAD_RESOURCE_ID

ULONG resource ID specific to hardware platform.

### -field SIOP_TYPE_USBAUD_FB_EP_USBD_ENDPOINT_DESCRIPTOR

Feedback Endpoint [USBD Endpoint Descriptor](../usbspec/ns-usbspec-_usb_endpoint_descriptor.md)

### -field SIOP_TYPE_USBAUD_FB_EP_USBD_ENDPOINT_OFFLOAD_INFORMATION

Feedback Endpoint [USBD Endpoint Offload Information](../usb/ns-usb-_usbd_endpoint_offload_information.md)

### -field SIOP_TYPE_USBAUD_FB_EP_USBAUDIO_TRANSPORT_RESOURCES

Feedback Endpoint [Sideband Audio EP transport resource](./ns-usbsidebandaudio-_sidebandaudio_ep_usbaudio_transport_resources.md)

### -field SIOP_TYPE_USBAUD_FB_EP_OFFLOAD_RESOURCE_ID

Feedback Endpoint ULONG resource ID specific to hardware platform.

### -field SIOP_TYPE_USBAUD_ENDPOINT_DESCRIPTOR_PER_FORMAT

USBD_ENDPOINT_DESCRIPTOR for specific format.

### -field SBUSBAUD_EP_TRANSPORT_RESOURCE_TYPE_INVALID

Unused

## -remarks

[IOCTL_SBAUD_GET_SIOP](../sidebandaudio/ni-sidebandaudio-ioctl_sbaud_get_siop.md) is defined with [METHOD_NEITHER](/windows-hardware/drivers/kernel/using-neither-buffered-nor-direct-i-o) buffering model. The requested resource information will be copied to the [Irp->UserBuffer](../wdm/ns-wdm-_irp.md).

## -see-also

[IOCTL_SBAUD_GET_SIOP](../sidebandaudio/ni-sidebandaudio-ioctl_sbaud_get_siop.md)

[usbsidebandaudio.h](index.md)