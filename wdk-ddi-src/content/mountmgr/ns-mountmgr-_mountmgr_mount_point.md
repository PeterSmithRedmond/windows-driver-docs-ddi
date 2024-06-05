---
UID: NS:mountmgr._MOUNTMGR_MOUNT_POINT
title: MOUNTMGR_MOUNT_POINT (mountmgr.h)
description: Learn about the MOUNTMGR_MOUNT_POINT structure.
tech.root: storage
ms.date: 06/04/2024
keywords: ["MOUNTMGR_MOUNT_POINT structure"]
ms.keywords: "*PMOUNTMGR_MOUNT_POINT, MOUNTMGR_MOUNT_POINT, MOUNTMGR_MOUNT_POINT structure [Storage Devices], PMOUNTMGR_MOUNT_POINT, PMOUNTMGR_MOUNT_POINT structure pointer [Storage Devices], _MOUNTMGR_MOUNT_POINT, mountmgr/MOUNTMGR_MOUNT_POINT, mountmgr/PMOUNTMGR_MOUNT_POINT, storage.mountmgr_mount_point, structs-mntmgr_88136173-0786-4d4e-80b7-77f523e8d125.xml"
req.header: mountmgr.h
req.include-header: Mountmgr.h
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
req.typenames: MOUNTMGR_MOUNT_POINT, *PMOUNTMGR_MOUNT_POINT
f1_keywords:
 - _MOUNTMGR_MOUNT_POINT
 - mountmgr/_MOUNTMGR_MOUNT_POINT
 - PMOUNTMGR_MOUNT_POINT
 - mountmgr/PMOUNTMGR_MOUNT_POINT
 - MOUNTMGR_MOUNT_POINT
 - mountmgr/MOUNTMGR_MOUNT_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mountmgr.h
api_name:
 - _MOUNTMGR_MOUNT_POINT
 - PMOUNTMGR_MOUNT_POINT
 - MOUNTMGR_MOUNT_POINT
---

## -description

The **MOUNTMGR_MOUNT_POINT** structure is used by mount manager clients in conjunction with an [**IOCTL_MOUNTMGR_QUERY_POINTS**](ni-mountmgr-ioctl_mountmgr_query_points.md) request to query the mount manager for all of the mount points (symbolic links) associated with a device. The mount manager responds by sending an array of **MOUNTMGR_MOUNT_POINT** structures containing the mount points.

## -struct-fields

### -field SymbolicLinkNameOffset

Contains an offset, in bytes, into the output buffer where the symbolic link is located.

### -field SymbolicLinkNameLength

Contains the length, in bytes, of the symbolic link.

### -field Reserved1

### -field UniqueIdOffset

Contains an offset, in bytes, into the output buffer where the unique ID is located.

### -field UniqueIdLength

Contains the length, in bytes, of the unique ID.

### -field Reserved2

### -field DeviceNameOffset

Contains an offset, in bytes, into the output buffer where the nonpersistent device name is located.

### -field DeviceNameLength

Contains the length, in bytes, of the nonpersistent device name.

### -field Reserved3

## -remarks

None of the names returned are NULL terminated, nor do the buffers require terminating NULL characters. The caller of [**IOCTL_MOUNTMGR_QUERY_POINTS**](ni-mountmgr-ioctl_mountmgr_query_points.md) is not required to provide data in all of the members of the MOUNTMGR_MOUNT_POINT structure, but empty members must have an offset of zero.

On input, offsets are from the beginning of the MOUNTMGR_MOUNT_POINT structure. On output offsets are from the beginning of the buffer. This is usually the same as the beginning of the [**MOUNTMGR_MOUNT_POINTS**](ns-mountmgr-_mountmgr_mount_points.md) container structure (as opposed to the embedded MOUNTMGR_MOUNT_POINT array instance).

The [**IOCTL_MOUNTMGR_QUERY_POINTS**](ni-mountmgr-ioctl_mountmgr_query_points.md) request is available in Windows 2000 and later operating systems.

For more information, see [Supporting Mount Manager Requests in a Storage Class Driver](/windows-hardware/drivers/storage/supporting-mount-manager-requests-in-a-storage-class-driver).

## -see-also

[**IOCTL_MOUNTMGR_QUERY_POINTS**](ni-mountmgr-ioctl_mountmgr_query_points.md)
