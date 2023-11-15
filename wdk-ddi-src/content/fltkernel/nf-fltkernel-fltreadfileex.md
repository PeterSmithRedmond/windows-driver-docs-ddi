---
UID: NF:fltkernel.FltReadFileEx
title: FltReadFileEx function (fltkernel.h)
description: Learn more about the FltReadFileEx function.
tech.root: ifsk
ms.date: 11/15/2023
keywords: ["FltReadFileEx function"]
ms.keywords: FltReadFileEx, FltReadFileEx function [Installable File System Drivers], fltkernel/FltReadFileEx, ifsk.fltreadfileex
req.header: fltkernel.h
req.include-header: Fltkernel.h
req.target-type: Universal
req.target-min-winverclnt: Windows 8
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
req.lib: FltMgr.lib
req.dll: Fltmgr.sys
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - FltReadFileEx
 - fltkernel/FltReadFileEx
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - fltmgr.sys
api_name:
 - FltReadFileEx
---

# FltReadFileEx function

## -description

**FltReadFileEx** reads data from an open file, stream, or device. This function extends [**FltReadFile**](nf-fltkernel-fltreadfile.md) to allow the optional use of an MDL for read data instead of a mapped buffer address.

## -parameters

### -param InitiatingInstance [in]

An opaque instance pointer for the minifilter driver instance that the operation is to be sent to. The instance must be attached to the volume where the file resides. This parameter is required and cannot be NULL.

### -param FileObject [in]

A pointer to a [**FILE_OBJECT**](../wdm/ns-wdm-_file_object.md) for the file that the data is to be read from. This file object must be currently open. Calling **FltReadFileEx** when the file object is not yet open or is no longer open (for example, in a pre-create or post-cleanup callback routine) causes the system to ASSERT on a checked build. This parameter is required and cannot be NULL.

### -param ByteOffset [in, optional]

Pointer to a caller-allocated variable that specifies the starting byte offset within the file where the read operation is to begin.

If **ByteOffset** is specified, the I/O is performed at that offset, regardless of the current value of the file object’s **CurrentByteOffset** field.

* If the file was opened for synchronous I/O (FO_SYNCHRONOUS_IO is set in the file object’s **Flags** field), the caller can set **ByteOffset->LowPart** to FILE_USE_FILE_POINTER_POSITION and **ByteOffset->HighPart** to -1 to have the I/O performed at the file object’s **CurrentByteOffset** field.
* If the file wasn't opened for synchronous I/O, using FILE_USE_FILE_POINTER_POSITION is an error.

If **ByteOffset** isn't specified:

* If the file wasn't opened for synchronous I/O, that is an error.
* Otherwise, the I/O is performed at the file object’s **CurrentByteOffset**.

If the file object was opened for synchronous I/O, the **CurrentByteOffset** field gets updated unless the caller passes the FLTFL_IO_OPERATION_DO_NOT_UPDATE_BYTE_OFFSET flag.

* Note: the file system still updates **CurrentByteOffset** in this case. Filter Manager saves the **CurrentByteOffset** value before sending the I/O down the stack and restores it when the I/O returns. From the perspective of the caller of **FltReadFileEx** (and filters at higher altitudes) the **CurrrentByteOffset** is not updated. But filters below the caller see the updated **CurrentByteOffset** value in their post-read/write callbacks.

If the file object wasn't opened for synchronous I/O, the **CurrentByteOffset** field isn't updated regardless of the state of the **ByteOffset** parameter.

### -param Length [in]

The size, in bytes, of the buffer that the **Buffer** parameter points to.

### -param Buffer [out]

A pointer to a caller-allocated buffer that receives the data that is read from the file. If an MDL is provided in **Mdl**, **Buffer** must be NULL.

### -param Flags [in]

A bitmask of flags that specify the type of read operation to be performed.

| Flag | Meaning |
| ---- | ------- |
| FLTFL_IO_OPERATION_DO_NOT_UPDATE_BYTE_OFFSET | Minifilter drivers can set this flag to specify that **FltReadFile** should not update the file object's **CurrentByteOffset** field. |
| FLTFL_IO_OPERATION_NON_CACHED | Minifilter drivers can set this flag to specify a noncached read, even if the file object was not opened with FILE_NO_INTERMEDIATE_BUFFERING. |
| FLTFL_IO_OPERATION_PAGING | Minifilter drivers can set this flag to specify a paging read. |
| FLTFL_IO_OPERATION_SYNCHRONOUS_PAGING | Minifilter drivers can set this flag to specify a synchronous paging I/O read. Minifilter drivers that set this flag must also set the FLTFL_IO_OPERATION_PAGING flag. Available starting in Windows Vista. |

### -param BytesRead [out, optional]

A pointer to a caller-allocated variable that receives the number of bytes read from the file. If **CallbackRoutine** is not NULL, this parameter is ignored. Otherwise, this parameter is optional and can be NULL.

### -param CallbackRoutine [in, optional]

Pointer to a [**PFLT_COMPLETED_ASYNC_IO_CALLBACK**](nc-fltkernel-pflt_completed_async_io_callback.md)-typed callback routine to call when the read operation is complete. This parameter is optional and can be NULL.

### -param CallbackContext [in, optional]

A context pointer to be passed to the **CallbackRoutine** if one is present. This parameter is optional and can be NULL. If **CallbackRoutine** is NULL, this parameter is ignored.

### -param Key [in, optional]

An optional key associated with a byte range lock.

### -param Mdl [in, optional]

An optional MDL that describes the memory where the data is read. If a buffer is provided in **Buffer** , then **Mdl** must be NULL.

## -returns

**FltReadFileEx** returns the NTSTATUS value that was returned by the file system.

## -remarks

A minifilter driver calls **FltReadFileEx** to read data from an open file.

**FltReadFileEx** creates a read request and sends it to the minifilter driver instances attached below the initiating instance, and to the file system. The specified instance and the instances attached above it do not receive the read request.

**FltReadFileEx** performs noncached I/O if either of the following is true:

* The caller set the FLTFL_IO_OPERATION_NON_CACHED flag in the **Flags** parameter.

* The file object was opened for noncached I/O. Usually, this is done by specifying the FILE_NO_INTERMEDIATE_BUFFERING **CreateOptions** flag in the preceding call to [**FltCreateFile**](nf-fltkernel-fltcreatefile.md), [**FltCreateFileEx**](nf-fltkernel-fltcreatefileex.md), or [**ZwCreateFile**](../wdm/nf-wdm-zwcreatefile.md).

Noncached I/O imposes the following restrictions on the parameter values passed to **FltReadFileEx**:

* The buffer that the **Buffer** parameter points to must be aligned in accordance with the alignment requirement of the underlying storage device. To allocate such an aligned buffer, call [**FltAllocatePoolAlignedWithTag**](nf-fltkernel-fltallocatepoolalignedwithtag.md).

* The byte offset that the **ByteOffset** parameter points to must be a nonnegative multiple of the volume's sector size.

* The length specified in the **Length** parameter must be a nonnegative multiple of the volume's sector size.

If an attempt is made to read beyond the end of the file, **FltReadFileEx** returns an error.

If the value of the **CallbackRoutine** parameter is not NULL, the read operation is performed asynchronously.

If the value of the **CallbackRoutine** parameter is NULL, the read operation is performed synchronously. That is, **FltReadFileEx** waits until the read operation is complete before returning. This is true even if the file object that **FileObject** points to was opened for asynchronous I/O.

If multiple threads call **FltReadFileEx** for the same file object, and the file object was opened for synchronous I/O, the filter manager does not attempt to serialize I/O on the file. In this respect, **FltReadFileEx** differs from [**ZwReadFile**](../wdm/nf-wdm-zwreadfile.md).

The **Mdl** parameter is provided as a convenience when a minifilter already has an MDL available. The MDL is used directly and the additional step of mapping an address for **Buffer** can be avoided.

## -see-also

[**FILE_OBJECT**](../wdm/ns-wdm-_file_object.md)

[**FltAllocatePoolAlignedWithTag**](nf-fltkernel-fltallocatepoolalignedwithtag.md)

[**FltCreateFile**](nf-fltkernel-fltcreatefile.md)

[**FltCreateFileEx**](nf-fltkernel-fltcreatefileex.md)

[**FltWriteFile**](nf-fltkernel-fltwritefile.md)

[**ObReferenceObjectByHandle**](../wdm/nf-wdm-obreferenceobjectbyhandle.md)

[**PFLT_COMPLETED_ASYNC_IO_CALLBACK**](nc-fltkernel-pflt_completed_async_io_callback.md)

[**ZwCreateFile**](../wdm/nf-wdm-zwcreatefile.md)

[**ZwReadFile**](../wdm/nf-wdm-zwreadfile.md)

[**ZwWriteFile**](../wdm/nf-wdm-zwwritefile.md)
