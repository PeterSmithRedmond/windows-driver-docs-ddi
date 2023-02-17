---
UID: NS:ufs.UFS_UNIT_DESCRIPTOR
title: UFS_UNIT_DESCRIPTOR (ufs.h)
description: The UFS_UNIT_DESCRIPTOR structure describes a generic unit descriptor.
old-location: storage\ufs_unit_descriptor.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["UFS_UNIT_DESCRIPTOR structure"]
ms.keywords: "*PUFS_UNIT_DESCRIPTOR, PUFS_UNIT_DESCRIPTOR, PUFS_UNIT_DESCRIPTOR structure pointer [Storage Devices], UFS_UNIT_DESCRIPTOR, UFS_UNIT_DESCRIPTOR structure [Storage Devices], storage.ufs_unit_descriptor, ufs/PUFS_UNIT_DESCRIPTOR, ufs/UFS_UNIT_DESCRIPTOR"
req.header: ufs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
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
req.typenames: UFS_UNIT_DESCRIPTOR, *PUFS_UNIT_DESCRIPTOR
f1_keywords:
 - PUFS_UNIT_DESCRIPTOR
 - ufs/PUFS_UNIT_DESCRIPTOR
 - UFS_UNIT_DESCRIPTOR
 - ufs/UFS_UNIT_DESCRIPTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ufs.h
api_name:
 - PUFS_UNIT_DESCRIPTOR
 - UFS_UNIT_DESCRIPTOR
---

# UFS_UNIT_DESCRIPTOR structure


## -description

The **UFS_UNIT_DESCRIPTOR** structure describes a generic unit descriptor.

## -struct-fields

### -field bLength

Specifies the length, in bytes, of this descriptor.

### -field bDescriptorIDN

Specifies the type of the descriptor. This descriptor will have a value of **UFS_DESC_UNIT_IDN**.

### -field bUnitIndex

Specifies unit index

### -field bLUEnable

Specifies if the logic unit number (LUN) is enabled. If **bLUEnable** is equal to 0x00, the logical unit is disabled.

### -field bBootLunID

### -field bLUWriteProtect

Specifies if the logical unit is write-protected. Contains one of the following values:

| Value | Description |
| ----- | ----------- |
| 0x00  | The logical unit is not write protected. |
| 0x01  | The logical unit is write protected. |
| 0x02  | The logical unit is permanently write protected. |

### -field bLUQueueDepth

Specifies the logical unit queue depth. Can be any value from 0x00 to 0xff.

### -field bPSASensitive

Specifies if the logical unit is sensitive to soldering. Contains one of the following values:

| Value | Description |
| ----- | ----------- |
| 0x00  | The logical unit is not sensitive to soldering. |
| 0x01  | The logical unit is sensitive to soldering. |

### -field bMemoryType

Specifies the desired memory type. The **wSupportedMemoryTypes** parameter in the [**UFS_GEOMETRY_DESCRIPTOR**](ns-ufs-ufs_geometry_descriptor.md) structure indicates which memory types are supported by the device.

### -field bDataReliability

Specifies if the device is protected against a power failure during a write operation to the logical unit.

### -field bLogicalBlockSize

Specifies the logical block size of the descriptor. Set the value of this equal to the corresponding value in **dOptimalLogicalBlockSize** of [**UFS_GEOMETRY_DESCRIPTOR**](ns-ufs-ufs_geometry_descriptor.md) for the specific logical unit memory type.

### -field qLogicalBlockCount

Specifies the total number of addressable logical blocks in the logical unit.

### -field dEraseBlockSize

Specifies the erase block size.

### -field bProvisioningType

Specifies the provisioning type.

### -field qPhyMemResourceCount

Specifies the total physical memory resources available in the logical unit.

### -field wContextCapabilities

Specifies the number of contexts to be supported in each logical unit.

### -field bLargeUnitGranularity_M1

Specifies the Large Unit granularity, minus one.

### -field wLUMaxActiveHPBRegions

### -field wHPBPinnedRegionStartIdx

### -field wNumHPBPinnedRegions

### -field Reserved

Reserved for future use.

## -remarks

**bPSASensitive** and **dEraseBlockSize** are updated automatically after device configuration.

## -see-also

[**UFS_GEOMETRY_DESCRIPTOR**](ns-ufs-ufs_geometry_descriptor.md)

[**UFS_RPMB_UNIT_DESCRIPTOR**](ns-ufs-ufs_rpmb_unit_descriptor.md)

