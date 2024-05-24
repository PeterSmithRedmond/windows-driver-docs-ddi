---
UID: NS:ntdddisk._DISK_PERFORMANCE
title: DISK_PERFORMANCE (ntdddisk.h)
description: Learn more about the DISK_PERFORMANCE structure.
tech.root: storage
ms.date: 05/24/2024
keywords: ["DISK_PERFORMANCE structure"]
ms.keywords: "*PDISK_PERFORMANCE, DISK_PERFORMANCE, DISK_PERFORMANCE structure [Storage Devices], PDISK_PERFORMANCE, PDISK_PERFORMANCE structure pointer [Storage Devices], _DISK_PERFORMANCE, ntdddisk/DISK_PERFORMANCE, ntdddisk/PDISK_PERFORMANCE, storage.disk_performance, structs-disk_64493b27-dce7-4976-9519-c7324bd09b69.xml"
req.header: ntdddisk.h
req.include-header: Ntdddisk.h
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
req.typenames: DISK_PERFORMANCE, *PDISK_PERFORMANCE
f1_keywords:
 - _DISK_PERFORMANCE
 - ntdddisk/_DISK_PERFORMANCE
 - PDISK_PERFORMANCE
 - ntdddisk/PDISK_PERFORMANCE
 - DISK_PERFORMANCE
 - ntdddisk/DISK_PERFORMANCE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntdddisk.h
api_name:
 - _DISK_PERFORMANCE
 - PDISK_PERFORMANCE
 - DISK_PERFORMANCE
---

# DISK_PERFORMANCE structure

## -description

The DISK_PERFORMANCE structure is used in conjunction with the [**IOCTL_DISK_PERFORMANCE**](ni-ntdddisk-ioctl_disk_performance.md) request to collect summary disk statistics for purposes of measuring disk performance.

## -struct-fields

### -field BytesRead

Contains a cumulative count of bytes read from the disk since the performance counters were enabled.

### -field BytesWritten

Contains a cumulative count of bytes written to the disk since the performance counters were enabled.

### -field ReadTime

Contains a cumulative time, expressed in increments of 100 nanoseconds, spent on disk reads since the performance counters were enabled.

### -field WriteTime

Contains a cumulative time, expressed in increments of 100 nanoseconds, spent on disk reads since the performance counters were enabled.

### -field IdleTime

Contains a cumulative time, expressed in increments of 100 nanoseconds, since the performance counters were enabled in which there was no disk activity.

### -field ReadCount

Contains the number of disk accesses for reads since the performance counters were enabled.

### -field WriteCount

Contains the number of disk accesses for writes since the performance counters were enabled.

### -field QueueDepth

Contains a snapshot of the number of queued disk I/O requests at the time that the query for performance statistics was performed.

### -field SplitCount

Contains the number of disk accesses by means of an associated IRP since the performance counters were enabled.

### -field QueryTime

Contains a timestamp indicating the system time at the moment that the query took place. System time is a count of 100-nanosecond intervals since January 1, 1601. System time is typically updated approximately every ten milliseconds. For more information about system time, see[**KeQuerySystemTime**](../wdm/nf-wdm-kequerysystemtime.md).

### -field StorageDeviceNumber

Contains a unique number assigned to every disk or volume across a particular storage type. The storage types are *disk.sys*, *ftdisk.sys*, and *dmio.sys*.

### -field StorageManagerName

Contains an 8-character string that indicates which device driver provided the performance statistics.

* In Windows 2000, this can be either "LogiDisk" for the driver *logidisk.sys* or "PhysDisk" for the driver *physdisk.sys*. These drivers collect performance statistics for devices and physical disks respectively.

* In Windows XP and later operating systems, this can be any of the following three strings: "FTDISK" for the driver *ftdisk.sys*, "DMIO" for the driver *dmio.sys*, or "PARTMGR" for the driver *partmgr.sys*. These three drivers collect performance statistics for basic disk volumes, dynamic disk volumes, and physical disks respectively. Note that these strings are 8-character case-sensitive strings with blank fill. For example, in the case of the string "FTDISK", the **StorageManagerName** character array should contain two trailing blanks ("FTDISK&nbsp;&nbsp;"), and in the case of the string "DMIO", the array should contain four trailing blanks ("DMIO&nbsp;&nbsp;&nbsp;&nbsp;").

## -remarks

Counting halts whenever the performance counters are disabled, but the counters are not reset, so the cumulative values assigned to the structure members might potentially reflect disk activity across several enablings and disablings of the counters.

## -see-also

[**IOCTL_DISK_PERFORMANCE**](ni-ntdddisk-ioctl_disk_performance.md)

[**IOCTL_DISK_PERFORMANCE_OFF**](ni-ntdddisk-ioctl_disk_performance_off.md)
