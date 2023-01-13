---
UID: NF:ntddk.IoGetConfigurationInformation
title: IoGetConfigurationInformation function (ntddk.h)
description: The IoGetConfigurationInformation function (ntddk.h) returns a pointer to the I/O manager's global configuration information structure.
tech.root: kernel
ms.date: 01/10/2023
keywords: ["IoGetConfigurationInformation function"]
ms.keywords: IoGetConfigurationInformation, IoGetConfigurationInformation routine [Kernel-Mode Driver Architecture], k104_5f9c4d01-9724-4e1d-8154-3737f0809068.xml, kernel.iogetconfigurationinformation, ntddk/IoGetConfigurationInformation
req.header: ntddk.h
req.include-header: Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt:
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: IrqlIoPassive5, PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - IoGetConfigurationInformation
 - ntddk/IoGetConfigurationInformation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - IoGetConfigurationInformation
---

## -description

The **IoGetConfigurationInformation** routine returns a pointer to the I/O manager's global configuration information structure, which contains the current values for how many physical disk, floppy, CD-ROM, tape, SCSI HBA, serial, and parallel devices have device objects created to represent them by drivers as they are loaded.

## -returns

**IoGetConfigurationInformation** returns a pointer to the configuration information structure. This structure is defined as follows:

```cpp
typedef struct _CONFIGURATION_INFORMATION {

    //
    // This field indicates the total number of disks in the system. This
    // number should be used by the driver to determine the names of new
    // disks. This field should be updated by the driver as it finds new
    // disks.
    //

    ULONG DiskCount;                // Count of hard disks thus far
    ULONG FloppyCount;              // Count of floppy disks thus far
    ULONG CdRomCount;               // Count of CD-ROM drives thus far
    ULONG TapeCount;                // Count of tape drives thus far
    ULONG ScsiPortCount;            // Count of SCSI port adapters thus far
    ULONG SerialCount;              // Count of serial devices thus far
    ULONG ParallelCount;            // Count of parallel devices thus far

    //
    // These next two fields indicate ownership of the two I/O address
    // spaces that are used by WD1003-compatible disk controllers.
    //

    BOOLEAN AtDiskPrimaryAddressClaimed;    // 0x1F0 - 0x1FF
    BOOLEAN AtDiskSecondaryAddressClaimed;  // 0x170 - 0x17F

    //
    // Indicates the structure version, as anything value beyond this will have been added.
    // Use the structure size as the version.
    //

    ULONG Version;

    //
    // Indicates the total number of medium changer devices in the system.
    // This field will be updated by the drivers as it determines that
    // new devices have been found and will be supported.
    //

    ULONG MediumChangerCount;

} CONFIGURATION_INFORMATION, *PCONFIGURATION_INFORMATION;
```

## -remarks

Certain types of device drivers can use the configuration information structure's values to construct device object names with appropriate digit suffixes when each driver creates its device objects. Note that the digit suffix for device object names is a zero-based count, while the counts maintained in the configuration information structure represent the number of device objects of a particular type already created. That is, the configuration information counts are one-based.

Any driver that calls **IoGetConfigurationInformation** must increment the count for its kind of device in this structure when it creates a device object to represent a physical device.

The system-supplied SCSI port driver supplies the count of SCSI HBAs present in the computer. SCSI class drivers can read this value to determine how many HBA-specific miniport drivers might control a SCSI bus with an attached device of the class driver's type.

The configuration information structure also contains a value indicating whether an already loaded driver has claimed either of the "AT" disk I/O address ranges.

## -see-also

[HalAssignSlotResources](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[HalGetBusData](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[HalGetBusDataByOffset](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[IoAssignResources](/windows-hardware/drivers/kernel/mmcreatemdl)

[IoQueryDeviceDescription](/windows-hardware/drivers/kernel/mmcreatemdl)

[IoReportResourceUsage](/windows-hardware/drivers/kernel/mmcreatemdl)
