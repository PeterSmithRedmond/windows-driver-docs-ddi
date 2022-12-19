---
UID: NF:wdm.ZwQueryInformationFile
title: ZwQueryInformationFile function (wdm.h)
description: The ZwQueryInformationFile routine returns various kinds of information about a file object.
old-location: kernel\zwqueryinformationfile.htm
tech.root: kernel
ms.date: 09/27/2021
keywords: ["ZwQueryInformationFile function"]
ms.keywords: NtQueryInformationFile, ZwQueryInformationFile, ZwQueryInformationFile routine [Kernel-Mode Driver Architecture], k111_822ab812-a644-4574-8d89-c4ebf5b17ea5.xml, kernel.zwqueryinformationfile, wdm/NtQueryInformationFile, wdm/ZwQueryInformationFile
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL (see Remarks section)
targetos: Windows
req.typenames: 
f1_keywords:
 - ZwQueryInformationFile
 - wdm/ZwQueryInformationFile
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - ZwQueryInformationFile
---

# ZwQueryInformationFile function

## -description

The **ZwQueryInformationFile** routine returns various kinds of information about a file object.

## -parameters

### -param FileHandle [in]

Handle to a file object. The handle is created by a successful call to [**ZwCreateFile**](../ntifs/nf-ntifs-ntcreatefile.md) or [**ZwOpenFile**](../ntifs/nf-ntifs-ntopenfile.md).

### -param IoStatusBlock [out]

Pointer to an [**IO_STATUS_BLOCK**](ns-wdm-_io_status_block.md) structure that receives the final completion status and information about the operation. The **Information** member receives the number of bytes that this routine actually writes to the **FileInformation** buffer.

### -param FileInformation [out]

Pointer to a caller-allocated buffer into which the routine writes the requested information about the file object. The **FileInformationClass** parameter specifies the type of information that the caller requests.

### -param Length [in]

The size, in bytes, of the buffer pointed to by **FileInformation**.

### -param FileInformationClass [in]

Specifies the type of information to be returned about the file, in the buffer that **FileInformation** points to. Device and intermediate drivers can specify any of the following [**FILE_INFORMATION_CLASS**](ne-wdm-_file_information_class.md) values.

| FILE_INFORMATION_CLASS value | Type of information returned |
| ---------------------------- | ---------------------------- |
| **FileBasicInformation** (4) | A [**FILE_BASIC_INFORMATION**](ns-wdm-_file_basic_information.md) structure. The caller must have opened the file with the FILE_READ_ATTRIBUTES flag specified in the **DesiredAccess** parameter. |
| **FileStandardInformation** (5) | A [**FILE_STANDARD_INFORMATION**](ns-wdm-_file_standard_information.md) structure. The caller can query this information as long as the file is open, without any particular requirements for **DesiredAccess**. |
| **FileInternalInformation** (6) | A [**FILE_INTERNAL_INFORMATION**](../ntifs/ns-ntifs-_file_internal_information.md) structure. This structure specifies a 64-bit file ID that uniquely identifies a file in NTFS. On other file systems, this file ID is not guaranteed to be unique. |
| **FileEaInformation** (7) | A [**FILE_EA_INFORMATION**](../ntifs/ns-ntifs-_file_ea_information.md) structure. This structure specifies the size of the extended attributes block that is associated with the file. |
| **FileAccessInformation** (8) | A [**FILE_ACCESS_INFORMATION**](../ntifs/ns-ntifs-_file_access_information.md) structure. This structure contains an access mask. For more information about access masks, see [**ACCESS_MASK**](/windows-hardware/drivers/kernel/access-mask). |
| **FileNameInformation** (9) | A [**FILE_NAME_INFORMATION**](../ntddk/ns-ntddk-_file_name_information.md) structure. The structure can contain the file's full path or only a portion of it. The caller can query this information as long as the file is open, without any particular requirements for **DesiredAccess**. For more information about the file-name syntax, see the Remarks section later in this topic. |
| **FilePositionInformation** (14) | A [**FILE_POSITION_INFORMATION**](ns-wdm-_file_position_information.md) structure. The caller must have opened the file with the **DesiredAccess** FILE_READ_DATA or FILE_WRITE_DATA flag specified in the **DesiredAccess** parameter, and with the FILE_SYNCHRONOUS_IO_ALERT or FILE_SYNCHRONOUS_IO_NONALERT flag specified in the **CreateOptions** parameter. |
| **FileModeInformation** (16) | A [**FILE_MODE_INFORMATION**](../ntifs/ns-ntifs-_file_mode_information.md) structure. This structure contains a set of flags that specify the mode in which the file can be accessed. These flags are a subset of the options that can be specified in the **CreateOptions** parameter of the [**IoCreateFile**](nf-wdm-iocreatefile.md) routine. |
| **FileAlignmentInformation** (17) | A [**FILE_ALIGNMENT_INFORMATION**](../ntddk/ns-ntddk-_file_alignment_information.md) structure. The caller can query this information as long as the file is open, without any particular requirements for **DesiredAccess*[***. This information is useful if the file was opened with the FILE_NO_INTERMEDIATE_BUFFERING flag specified in the **CreateOptions** parameter. |
| **FileAllInformation** (18) | A [**FILE_ALL_INFORMATION**](../ntifs/ns-ntifs-_file_all_information.md) structure. By combining several file-information structures into a single structure, **FILE_ALL_INFORMATION** reduces the number of queries required to obtain information about a file. |
| **FileNetworkOpenInformation** (34) | A [**FILE_NETWORK_OPEN_INFORMATION**](ns-wdm-_file_network_open_information.md) structure. The caller must have opened the file with the FILE_READ_ATTRIBUTES flag specified in the **DesiredAccess** parameter. |
| **FileAttributeTagInformation** (35) | A [**FILE_ATTRIBUTE_TAG_INFORMATION**](../ntddk/ns-ntddk-_file_attribute_tag_information.md) structure. The caller must have opened the file with the FILE_READ_ATTRIBUTES flag specified in the **DesiredAccess** parameter. |
| **FileIoPriorityHintInformation** (43) | A [**FILE_IO_PRIORITY_HINT_INFORMATION**](ns-wdm-_file_io_priority_hint_information.md) structure. The caller must have opened the file with the FILE_READ_DATA flag specified in the **DesiredAccess** parameter. |
| **FileIsRemoteDeviceInformation** (51) | A [**FILE_IS_REMOTE_DEVICE_INFORMATION**](ns-wdm-_file_is_remote_device_information.md) structure. The caller can query this information as  long as the file is open, without any particular requirements for **DesiredAccess**. |
| **FileKnownFolderInformation** (76) | A [**FILE_KNOWN_FOLDER_INFORMATION**](../ntifs/ns-ntifs-file_known_folder_information.md) structure. Available starting in Windows Server 2022. |

## -returns

**ZwQueryInformationFile** returns STATUS_SUCCESS or an appropriate NTSTATUS error code.

## -remarks

**ZwQueryInformationFile** returns information about the specified file object. Note that it returns zero in any member of a **FILE_*XXX*_INFORMATION** structure that is not supported by a particular device or file system.

When **FileInformationClass** = **FileNameInformation**, the file name is returned in the [**FILE_NAME_INFORMATION**](../ntddk/ns-ntddk-_file_name_information.md) structure. The precise syntax of the file name depends on a number of factors:

* *If you opened the file by submitting a full path to [**ZwCreateFile**](../ntifs/nf-ntifs-ntcreatefile.md), **ZwQueryInformationFile** returns that full path.

*If the **ObjectAttributes->RootDirectory** handle was opened by name in a call to **ZwCreateFile**, and subsequently the file was opened by **ZwCreateFile** relative to this root-directory handle, **ZwQueryInformationFile** returns the full path.

* If the **ObjectAttributes->RootDirectory** handle was opened by file ID (using the FILE_OPEN_BY_FILE_ID flag) in a call to **ZwCreateFile**, and subsequently the file was opened by **ZwCreateFile** relative to this root-directory handle, **ZwQueryInformationFile** returns the relative path.

* However, if the user has [**SeChangeNotifyPrivilege**](/windows/win32/secauthz/privilege-constants), **ZwQueryInformationFile** returns the full path in all cases.

* If only the relative path is returned, the file name string will not begin with a backslash.

* If the full path and file name are returned, the string will begin with a single backslash, regardless of its location. Thus the file C:\dir1\dir2\filename.ext will appear as \dir1\dir2\filename.ext, while the file \\server\share\dir1\dir2\filename.ext will appear as \server\share\dir1\dir2\filename.ext.

If **ZwQueryInformationFile** fails because of a buffer overflow, drivers that implement **FileNameInformation** should return as many WCHAR characters of the file name as will fit in the buffer and specify the full length that is required in the **FileNameLength** parameter of the [**FILE_NAME_INFORMATION**](../ntddk/ns-ntddk-_file_name_information.md) structure. You should reissue the query by using the file name length so that you can retrieve the full file name. Drivers that do not follow this pattern might require a gradual increase in length until they retrieve the full file name. For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).

Callers of **ZwQueryInformationFile** must be running at IRQL = PASSIVE_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).

> [!NOTE]
>
> If the call to this function occurs in user mode, you should use the name "**NtQueryInformationFile**" instead of "**ZwQueryInformationFile**".

For calls from kernel-mode drivers, the **Nt*Xxx*** and **Zw*Xxx*** versions of a Windows Native System Services routine can behave differently in the way that they handle and interpret input parameters. For more information about the relationship between the **Nt**Xxx**** and **Zw**Xxx**** versions of a routine, see [Using Nt and Zw Versions of the Native System Services Routines](/windows-hardware/drivers/kernel/using-nt-and-zw-versions-of-the-native-system-services-routines).

## -see-also

[**FILE_ACCESS_INFORMATION**](../ntifs/ns-ntifs-_file_access_information.md)

[**FILE_ALIGNMENT_INFORMATION**](../ntddk/ns-ntddk-_file_alignment_information.md)

[**FILE_ALL_INFORMATION**](../ntifs/ns-ntifs-_file_all_information.md)

[**FILE_ATTRIBUTE_TAG_INFORMATION**](../ntddk/ns-ntddk-_file_attribute_tag_information.md)

[**FILE_BASIC_INFORMATION**](ns-wdm-_file_basic_information.md)

[**FILE_EA_INFORMATION**](../ntifs/ns-ntifs-_file_ea_information.md)

[**FILE_INTERNAL_INFORMATION**](../ntifs/ns-ntifs-_file_internal_information.md)

[**FILE_IO_PRIORITY_HINT_INFORMATION**](ns-wdm-_file_io_priority_hint_information.md)

[**FILE_IS_REMOTE_DEVICE_INFORMATION**](ns-wdm-_file_is_remote_device_information.md)

[**FILE_MODE_INFORMATION**](../ntifs/ns-ntifs-_file_mode_information.md)

[**FILE_NAME_INFORMATION**](../ntddk/ns-ntddk-_file_name_information.md)

[**FILE_NETWORK_OPEN_INFORMATION**](ns-wdm-_file_network_open_information.md)

[**FILE_POSITION_INFORMATION**](ns-wdm-_file_position_information.md)

[**FILE_STANDARD_INFORMATION**](ns-wdm-_file_standard_information.md)

[**ZwCreateFile**](../ntifs/nf-ntifs-ntcreatefile.md)

[**ZwSetInformationFile**](../ntifs/nf-ntifs-ntsetinformationfile.md)
