---
UID: NI:hidclass.IOCTL_HID_GET_MANUFACTURER_STRING
title: IOCTL_HID_GET_MANUFACTURER_STRING (hidclass.h)
description: The IOCTL_HID_GET_MANUFACTURER_STRING request obtains a top-level collection's embedded string that identifies the manufacturer of the device.
old-location: hid\ioctl_hid_get_manufacturer_string.htm
tech.root: hid
ms.date: 04/30/2018
keywords: ["IOCTL_HID_GET_MANUFACTURER_STRING IOCTL"]
ms.keywords: IOCTL_HID_GET_MANUFACTURER_STRING, IOCTL_HID_GET_MANUFACTURER_STRING control, IOCTL_HID_GET_MANUFACTURER_STRING control code [Human Input Devices], hid.ioctl_hid_get_manufacturer_string, hidclass/IOCTL_HID_GET_MANUFACTURER_STRING, hidioreq_05724f70-c708-4f9a-ba51-fa2edabf56ed.xml
req.header: hidclass.h
req.include-header: Hidclass.h
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
 - IOCTL_HID_GET_MANUFACTURER_STRING
 - hidclass/IOCTL_HID_GET_MANUFACTURER_STRING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - hidclass.h
api_name:
 - IOCTL_HID_GET_MANUFACTURER_STRING
---

# IOCTL_HID_GET_MANUFACTURER_STRING IOCTL

## -description

The IOCTL_HID_GET_MANUFACTURER_STRING request obtains a [top-level collection's](/windows-hardware/drivers/hid/top-level-collections) embedded string that identifies the manufacturer of the device. The retrieved string is a NULL-terminated wide character string in a human-readable format.

For general information about HIDClass devices see [HID Collections](/windows-hardware/drivers/hid/hid-collections).

## -ioctlparameters

### -ioctl-major-code

### -input-buffer

**Parameters.DeviceIoControl.OutputBufferLength** in the I/O stack location of the IRP indicates the size, in bytes, of the output buffer. If the output buffer is not large enough to hold the entire NULL-terminated embedded string, the request returns nothing in the output buffer.

### -input-buffer-length

The maximum possible number of characters in an embedded string is device specific. For USB devices, the maximum string length is 126 wide characters (not including the terminating NULL character).

### -output-buffer

**Irp->MdlAddress** points to a buffer to receive the manufacturer ID (a NULL-terminated wide character string).

### -output-buffer-length

The length of a NULL-terminated wide character string. The supplied buffer must be <= 4093 bytes (2^12 – 3).

### -in-out-buffer

### -inout-buffer-length

### -status-block

The HID class driver sets the following fields of **Irp->IoStatus**:

- **Information** is set to the number of bytes transferred from the device.

- **Status** is set to STATUS_SUCCESS if the transfer completed without error. Otherwise, it is set to an appropriate NTSTATUS error code.

## -see-also

[HidD_GetIndexedString](../hidsdi/nf-hidsdi-hidd_getindexedstring.md)

[HidD_GetManufacturerString](../hidsdi/nf-hidsdi-hidd_getmanufacturerstring.md)

[HidD_GetPhysicalDescriptor](../hidsdi/nf-hidsdi-hidd_getphysicaldescriptor.md)

[HidD_GetProductString](../hidsdi/nf-hidsdi-hidd_getproductstring.md)

[HidD_GetSerialNumberString](../hidsdi/nf-hidsdi-hidd_getserialnumberstring.md)

[IOCTL_HID_GET_INDEXED_STRING](./ni-hidclass-ioctl_hid_get_indexed_string.md)

[IOCTL_HID_GET_PRODUCT_STRING](./ni-hidclass-ioctl_hid_get_product_string.md)

[IOCTL_HID_GET_SERIALNUMBER_STRING](./ni-hidclass-ioctl_hid_get_serialnumber_string.md)