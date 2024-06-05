---
UID: NS:mountdev._MOUNTDEV_UNIQUE_ID
title: MOUNTDEV_UNIQUE_ID (mountdev.h)
description: Learn more about the MOUNTDEV_UNIQUE_ID structure.
tech.root: storage
ms.date: 06/04/2024
keywords: ["MOUNTDEV_UNIQUE_ID structure"]
ms.keywords: "*PMOUNTDEV_UNIQUE_ID, MOUNTDEV_UNIQUE_ID, MOUNTDEV_UNIQUE_ID structure [Storage Devices], PMOUNTDEV_UNIQUE_ID, PMOUNTDEV_UNIQUE_ID structure pointer [Storage Devices], _MOUNTDEV_UNIQUE_ID, mountdev/MOUNTDEV_UNIQUE_ID, mountdev/PMOUNTDEV_UNIQUE_ID, storage.mountdev_unique_id, structs-mntmgr_424fff73-7b72-4068-b25b-00225f69b159.xml"
req.header: mountdev.h
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
req.typenames: MOUNTDEV_UNIQUE_ID, *PMOUNTDEV_UNIQUE_ID
f1_keywords:
 - _MOUNTDEV_UNIQUE_ID
 - mountdev/_MOUNTDEV_UNIQUE_ID
 - PMOUNTDEV_UNIQUE_ID
 - mountdev/PMOUNTDEV_UNIQUE_ID
 - MOUNTDEV_UNIQUE_ID
 - mountdev/MOUNTDEV_UNIQUE_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mountdev.h
api_name:
 - _MOUNTDEV_UNIQUE_ID
 - PMOUNTDEV_UNIQUE_ID
 - MOUNTDEV_UNIQUE_ID
---

## -description

The **MOUNTDEV_UNIQUE_ID** structure contains a unique volume ID that a mount manager client provides to the mount manager in response to an [IOCTL_MOUNTDEV_QUERY_UNIQUE_ID](ni-mountdev-ioctl_mountdev_query_unique_id.md) request.

## -struct-fields

### -field UniqueIdLength

The length of the unique volume ID, in bytes.

### -field UniqueId

Array of bytes that specify the unique volume ID.

## -remarks

For a discussion of unique volume IDs and how the mount manager uses them, see [Supporting Mount Manager Requests in a Storage Class Driver](/windows-hardware/drivers/storage/supporting-mount-manager-requests-in-a-storage-class-driver).

As a best practice, the implementer must not thread synchronize and must not make blocking and/or Interprocess Communication (IPC) function calls.

## -see-also

[IOCTL_MOUNTDEV_QUERY_UNIQUE_ID](ni-mountdev-ioctl_mountdev_query_unique_id.md)
