---
UID: NS:ntifs._FILE_ALLOCATION_INFORMATION
title: FILE_ALLOCATION_INFORMATION (ntifs.h)
description: Learn more about the FILE_ALLOCATION_INFORMATION structure.
tech.root: ifsk
ms.date: 09/27/2023
keywords: ["FILE_ALLOCATION_INFORMATION structure"]
ms.keywords: "*PFILE_ALLOCATION_INFORMATION, FILE_ALLOCATION_INFORMATION, FILE_ALLOCATION_INFORMATION structure [Installable File System Drivers], PFILE_ALLOCATION_INFORMATION, PFILE_ALLOCATION_INFORMATION structure pointer [Installable File System Drivers], _FILE_ALLOCATION_INFORMATION, fileinformationstructures_79d60e3b-f403-46d8-b600-62aeddcb88e0.xml, ifsk.file_allocation_information, ntifs/FILE_ALLOCATION_INFORMATION, ntifs/PFILE_ALLOCATION_INFORMATION"
req.header: ntifs.h
req.include-header: Ntifs.h, Fltkernel.h
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
req.typenames: FILE_ALLOCATION_INFORMATION, *PFILE_ALLOCATION_INFORMATION
f1_keywords:
 - _FILE_ALLOCATION_INFORMATION
 - ntifs/_FILE_ALLOCATION_INFORMATION
 - PFILE_ALLOCATION_INFORMATION
 - ntifs/PFILE_ALLOCATION_INFORMATION
 - FILE_ALLOCATION_INFORMATION
 - ntifs/FILE_ALLOCATION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - _FILE_ALLOCATION_INFORMATION
 - PFILE_ALLOCATION_INFORMATION
 - FILE_ALLOCATION_INFORMATION
---

# FILE_ALLOCATION_INFORMATION structure

## -description

The **FILE_ALLOCATION_INFORMATION** structure is used to set the allocation size for a file.

## -struct-fields

### -field AllocationSize

File allocation size, in bytes. Usually this value is a multiple of the sector or cluster size of the underlying physical device.

## -remarks

This operation can be performed in either of the following ways:

* Call [**FltSetInformationFile**](../fltkernel/nf-fltkernel-fltsetinformationfile.md) or [**ZwSetInformationFile**](nf-ntifs-ntsetinformationfile.md), passing FileAllocationInformation as the value of **FileInformationClass** and passing a caller-allocated, FILE_ALLOCATION_INFORMATION-structured buffer as the value of **FileInformation**. The **FileHandle** parameter specifies the file whose allocation size is to be set.

* Create an IRP with major function code IRP_MJ_SET_INFORMATION.

This operation is valid only for files. It is undefined for directories.

File system minifilters must use [**FltSetInformationFile**](../fltkernel/nf-fltkernel-fltsetinformationfile.md), not [**ZwSetInformationFile**](nf-ntifs-ntsetinformationfile.md), to set the allocation size for a file.

FILE_WRITE_DATA access is required to set this information.

A file's allocation size and end-of-file position are independent of each other, with the following exception: The end-of-file position must always be less than or equal to the allocation size. If the allocation size is set to a value that is less than the end-of-file position, the end-of-file position is automatically adjusted to match the allocation size.

The size of the **FileInformation** buffer passed to [**FltSetInformationFile**](../fltkernel/nf-fltkernel-fltsetinformationfile.md) or [**ZwSetInformationFile**](nf-ntifs-ntsetinformationfile.md) must be >= ```sizeof(FILE_ALLOCATION_INFORMATION)```.

This structure must be aligned on a LONGLONG (8-byte) boundary.

## -see-also

[**FILE_END_OF_FILE_INFORMATION**](../ntddk/ns-ntddk-_file_end_of_file_information.md)

[**FltSetInformationFile**](../fltkernel/nf-fltkernel-fltsetinformationfile.md)

[**IRP_MJ_SET_INFORMATION**](/windows-hardware/drivers/ifs/irp-mj-set-information)

[**ZwSetInformationFile**](nf-ntifs-ntsetinformationfile.md)
