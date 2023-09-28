---
UID: NS:ntifs._FILE_INTERNAL_INFORMATION
title: FILE_INTERNAL_INFORMATION (ntifs.h)
description: Learn more about FILE_INTERNAL_INFORMATION structure.
tech.root: ifsk
ms.date: 09/27/2023
keywords: ["FILE_INTERNAL_INFORMATION structure"]
ms.keywords: "*PFILE_INTERNAL_INFORMATION, FILE_INTERNAL_INFORMATION, FILE_INTERNAL_INFORMATION structure [Installable File System Drivers], PFILE_INTERNAL_INFORMATION, PFILE_INTERNAL_INFORMATION structure pointer [Installable File System Drivers], _FILE_INTERNAL_INFORMATION, fileinformationstructures_7be724e0-06ec-4555-bcce-14926b7d92df.xml, ifsk.file_internal_information, ntifs/FILE_INTERNAL_INFORMATION, ntifs/PFILE_INTERNAL_INFORMATION"
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
req.typenames: FILE_INTERNAL_INFORMATION, *PFILE_INTERNAL_INFORMATION
f1_keywords:
 - _FILE_INTERNAL_INFORMATION
 - ntifs/_FILE_INTERNAL_INFORMATION
 - PFILE_INTERNAL_INFORMATION
 - ntifs/PFILE_INTERNAL_INFORMATION
 - FILE_INTERNAL_INFORMATION
 - ntifs/FILE_INTERNAL_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - _FILE_INTERNAL_INFORMATION
 - PFILE_INTERNAL_INFORMATION
 - FILE_INTERNAL_INFORMATION
---

# FILE_INTERNAL_INFORMATION structure

## -description

The **FILE_INTERNAL_INFORMATION** structure is used to query for the file system's 8-byte file reference number for a file.

## -struct-fields

### -field IndexNumber

The 8-byte file reference number for the file. This number is assigned by the file system and is file-system-specific. (Note that this is not the same as the 16-byte "file object ID" that was added to NTFS for Microsoft Windows 2000.)

## -remarks

This information can be queried in either of the following ways:

* Call [**FltQueryInformationFile**](../fltkernel/nf-fltkernel-fltqueryinformationfile.md) or [**ZwQueryInformationFile**](nf-ntifs-ntqueryinformationfile.md), passing FileInternalInformation as the value of **FileInformationClass** and passing a caller-allocated, FILE_INTERNAL_INFORMATION-structured buffer as the value of **FileInformation**.

* Create an IRP with major function code [**IRP_MJ_QUERY_INFORMATION**](/windows-hardware/drivers/ifs/irp-mj-query-information).

No specific access rights are required to query this information.

The **IndexNumber** member of the FILE_INTERNAL_INFORMATION structure is the same as the **FileId** member of the FILE_ID_BOTH_DIR_INFORMATION and FILE_ID_FULL_DIR_INFORMATION structures.

File reference numbers, also called file IDs, are guaranteed to be unique only within a static file system. They are not guaranteed to be unique over time, because file systems are free to reuse them. Nor are they guaranteed to remain constant. For example, the FAT file system generates the file reference number for a file from the byte offset of the file's directory entry record (DIRENT) on the disk. Defragmentation can change this byte offset. Thus a FAT file reference number can change over time.

The size of the buffer passed in the **FileInformation** parameter to [**FltQueryInformationFile**](../fltkernel/nf-fltkernel-fltqueryinformationfile.md) or [**ZwQueryInformationFile**](nf-ntifs-ntqueryinformationfile.md) must be at least ```sizeof(FILE_INTERNAL_INFORMATION)```.

This structure must be aligned on a LONGLONG (8-byte) boundary.

## -see-also

[**FILE_ID_BOTH_DIR_INFORMATION**](ns-ntifs-_file_id_both_dir_information.md)

[**FILE_ID_FULL_DIR_INFORMATION**](ns-ntifs-_file_id_full_dir_information.md)

[**FILE_OBJECTID_INFORMATION**](ns-ntifs-_file_objectid_information.md)

[**FltQueryInformationFile**](../fltkernel/nf-fltkernel-fltqueryinformationfile.md)

[**ZwQueryInformationFile**](nf-ntifs-ntqueryinformationfile.md)
