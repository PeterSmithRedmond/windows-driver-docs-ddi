---
UID: NF:fltkernel.FltAllocateContext
title: FltAllocateContext function (fltkernel.h)
description: Learn more about the FltAllocateContext function.
old-location: ifsk\fltallocatecontext.htm
tech.root: ifsk
ms.date: 05/04/2023
keywords: ["FltAllocateContext function"]
ms.keywords: FltAllocateContext, FltAllocateContext routine [Installable File System Drivers], FltApiRef_a_to_d_dcc03d8c-1f61-4afb-8774-f98951ebfb1f.xml, fltkernel/FltAllocateContext, ifsk.fltallocatecontext
req.header: fltkernel.h
req.include-header: Fltkernel.h
req.target-type: Universal
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
req.lib: FltMgr.lib
req.dll: Fltmgr.sys
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - FltAllocateContext
 - fltkernel/FltAllocateContext
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - fltmgr.sys
api_name:
 - FltAllocateContext
---

# FltAllocateContext function

## -description

The **FltAllocateContext** routine allocates a context structure for a specified context type.

## -parameters

### -param Filter [in]

Opaque filter pointer for the caller. This parameter is required and cannot be **NULL**.

### -param ContextType [in]

A **FLT_CONTEXT_TYPE** value that indicates the type of context to allocate. **ContextType** can be one of the following:

| Value  | Meaning |
| ------ | ------- |
| FLT_VOLUME_CONTEXT       (0x0002) | Allocate a volume context. |
| FLT_FILE_CONTEXT         (0x0004) | Allocate a file context.   |
| FLT_STREAM_CONTEXT       (0x0008) | Allocate a stream context.  |
| FLT_STREAMHANDLE_CONTEXT (0x0010) | Allocate a stream handle context.  |
| FLT_TRANSACTION_CONTEXT  (0x0020) | Allocate a transaction context.  |
| FLT_SECTION_CONTEXT      (0x0040) | Allocate a section context. Available starting in Windows 8. |

### -param ContextSize [in]

The size, in bytes, of the portion of the context defined by the minifilter driver. Must be greater than zero and less than or equal to **MAXUSHORT**; for fixed-size contexts, must be less than or equal to the **Size** specified in the [**FLT_CONTEXT_REGISTRATION**](ns-fltkernel-_flt_context_registration.md) structure. A minifilter uses this portion of the context to maintain context information specific to itself. *FltMgr* treats this portion of the context structure as opaque. This parameter is required and cannot be zero.

### -param PoolType [in]

The type of pool to allocate. This parameter is required and must be one of the following. See [**POOL_TYPE**](../wdm/ne-wdm-_pool_type.md) for a detailed description of each type. See Remarks for more information.

| Value  | Meaning |
| ------ | ------- |
| **NonPagedPool**   | Nonpageable system memory. **PoolType** must be **NonPagedPool** if **ContextType** is FLT_VOLUME_CONTEXT.|
| **PagedPool**      | Pageable system memory. |
| **NonPagedPoolNx** | No-execute (NX) nonpaged pool. |

### -param ReturnedContext [out]

Pointer to a caller-allocated variable that receives the address of the newly allocated context. The caller is responsible for calling [**FltReleaseContext**](nf-fltkernel-fltreleasecontext.md) to release this context when it is no longer needed.

## -returns

**FltAllocateContext** returns **STATUS_SUCCESS** or an appropriate **NTSTATUS** value, such as one of the following:

| Return code | Description |
| ----------- | ----------- |
| STATUS_FLT_CONTEXT_ALLOCATION_NOT_FOUND | The allocation information for the context of the specified type was not provided at the time of filter registration. OR, for fixed-size contexts, the requested **ContextSize** is greater than the **Size** specified in the [**FLT_CONTEXT_REGISTRATION**](ns-fltkernel-_flt_context_registration.md) structure for the specified **ContextType**. |
| STATUS_FLT_DELETING_OBJECT | The minifilter driver that is specified in the **Filter** parameter is being torn down. This is an error code. |
| STATUS_INSUFFICIENT_RESOURCES | **FltAllocateContext** encountered a pool allocation failure. This is an error code. |
| STATUS_INVALID_BUFFER_SIZE | **ContextSize** cannot be greater than **MAXUSHORT**. This is an error code. |
| STATUS_INVALID_PARAMETER | An invalid value was specified for the **ContextType** or the **ContextSize** parameter. This is an error code. |
| STATUS_NOT_SUPPORTED | The file system does not support per-stream contexts. This is an error code. |

## -remarks

For more information about contexts, see [About minifilter contexts](/windows-hardware/drivers/ifs/managing-contexts-in-a-minifilter-driver).

**FltAllocateContext** allocates a context of the specified type from the specified pool. Starting in Windows 11, whether the memory that **ReturnedContext** points to is zeroed depends as follows:

* The memory is guaranteed to be zeroed for variable-sized contexts.
* The memory content is implementation-defined for fixed-sized contexts allocated by a caller-provided callback function.
* Otherwise, the memory can't be assumed to be zeroed for fixed-sized contexts because of lookaside list behavior. That is, an entry returned from the lookaside list might not be zeroed if it is memory that was previously freed to the lookaside list as opposed to a fresh allocation.

Before Windows 11, the contents of the returned context are not zeroed.

Setting **PoolType** to an invalid value can result in unexpected behavior such as causing lookaside lists to be bypassed, resulting in the loss of the performance benefits of lookaside lists. For contexts that have a **ContextAllocateCallback** callback function, the behavior due to an invalid **PoolType** is implementation-dependent.

After the context is allocated, it can be set on an object by passing the **ReturnedContext** pointer to the appropriate set-context routine from the following table.

| Context Type | Set-Context Routine |
| ------------ | ------------------- |
| FLT_FILE_CONTEXT | [**FltSetFileContext**](nf-fltkernel-fltsetfilecontext.md) (starting with Windows Vista) |
| FLT_INSTANCE_CONTEXT | [**FltSetInstanceContext**](nf-fltkernel-fltsetinstancecontext.md) |
| FLT_SECTION_CONTEXT | [**FltCreateSectionForDataScan**](nf-fltkernel-fltcreatesectionfordatascan.md) (starting with Windows 8) |
| FLT_STREAM_CONTEXT | [**FltSetStreamContext**](nf-fltkernel-fltsetstreamcontext.md) |
| FLT_STREAMHANDLE_CONTEXT | [**FltSetStreamHandleContext**](nf-fltkernel-fltsetstreamhandlecontext.md) |
| FLT_TRANSACTION_CONTEXT | [**FltSetTransactionContext**](nf-fltkernel-fltsettransactioncontext.md) (starting with Windows Vista) |
| FLT_VOLUME_CONTEXT | [**FltSetVolumeContext**](nf-fltkernel-fltsetvolumecontext.md) |

When a minifilter driver calls [**FltRegisterFilter**](nf-fltkernel-fltregisterfilter.md) from its **DriverEntry** routine, it must register each context type that it uses. For more information, see the reference entry for the [**FLT_CONTEXT_REGISTRATION**](ns-fltkernel-_flt_context_registration.md) structure, and [Registering context types](/windows-hardware/drivers/ifs/registering-context-types).

**FltAllocateContext** does not initialize the contents of the portion of the context structure specific to the minifilter driver.

To get the context for an object, call [**FltGetContexts**](nf-fltkernel-fltgetcontexts.md) or the appropriate get-context routine from the following table.

| Context Type | Get-Context Routine |
| ------------ | ------------------- |
| FLT_FILE_CONTEXT | [**FltGetFileContext**](nf-fltkernel-fltgetfilecontext.md) (starting with Windows Vista) |
| FLT_INSTANCE_CONTEXT | [**FltGetInstanceContext**](nf-fltkernel-fltgetinstancecontext.md) |
| FLT_SECTION_CONTEXT | [**FltGetSectionContext**](nf-fltkernel-fltgetsectioncontext.md) (starting with Windows 8) |
| FLT_STREAM_CONTEXT | [**FltGetStreamContext**](nf-fltkernel-fltgetstreamcontext.md) |
| FLT_STREAMHANDLE_CONTEXT | [**FltGetStreamHandleContext**](nf-fltkernel-fltgetstreamhandlecontext.md) |
| FLT_TRANSACTION_CONTEXT | [**FltGetTransactionContext**](nf-fltkernel-fltgettransactioncontext.md) (starting with Windows Vista ) |
| FLT_VOLUME_CONTEXT | [**FltGetVolumeContext**](nf-fltkernel-fltgetvolumecontext.md) |

Contexts are reference-counted, and on a successful return from **FltAllocateContext**, the context pointed to by **ReturnedContext** has been initialized to have a reference count of 1. A context is freed automatically when its reference count reaches zero. To increment the reference count on a context, call [**FltReferenceContext**](nf-fltkernel-fltreferencecontext.md).

To decrement the reference count on a context, call [**FltReleaseContext**](nf-fltkernel-fltreleasecontext.md).

Because contexts are reference-counted, it is not usually necessary to delete them. To delete a context explicitly, call [**FltDeleteContext**](nf-fltkernel-fltdeletecontext.md) or the appropriate delete-context routine from the following table.

| Context Type | Delete-Context Routine |
| ------------ | ---------------------- |
| FLT_FILE_CONTEXT | [**FltDeleteFileContext**](nf-fltkernel-fltdeletefilecontext.md) (starting with Windows Vista) |
| FLT_INSTANCE_CONTEXT | [**FltDeleteInstanceContext**](nf-fltkernel-fltdeleteinstancecontext.md) |
| FLT_SECTION_CONTEXT | [**FltCloseSectionForDataScan**](nf-fltkernel-fltclosesectionfordatascan.md) (starting with Windows 8) |
| FLT_STREAM_CONTEXT | [**FltDeleteStreamContext**](nf-fltkernel-fltdeletestreamcontext.md) |
| FLT_STREAMHANDLE_CONTEXT | [**FltDeleteStreamHandleContext**](nf-fltkernel-fltdeletestreamhandlecontext.md) |
| FLT_TRANSACTION_CONTEXT | [**FltDeleteTransactionContext**](nf-fltkernel-fltdeletetransactioncontext.md) (starting with Windows Vista) |
| FLT_VOLUME_CONTEXT | [**FltDeleteVolumeContext**](nf-fltkernel-fltdeletevolumecontext.md) |

## -see-also

[**FLT_CONTEXT_REGISTRATION**](ns-fltkernel-_flt_context_registration.md)

[**FltCloseSectionForDataScan**](nf-fltkernel-fltclosesectionfordatascan.md)

[**FltCreateSectionForDataScan**](nf-fltkernel-fltcreatesectionfordatascan.md)

[**FltDeleteContext**](nf-fltkernel-fltdeletecontext.md)

[**FltDeleteFileContext**](nf-fltkernel-fltdeletefilecontext.md)

[**FltDeleteInstanceContext**](nf-fltkernel-fltdeleteinstancecontext.md)

[**FltDeleteStreamContext**](nf-fltkernel-fltdeletestreamcontext.md)

[**FltDeleteStreamHandleContext**](nf-fltkernel-fltdeletestreamhandlecontext.md)

[**FltDeleteTransactionContext**](nf-fltkernel-fltdeletetransactioncontext.md)

[**FltDeleteVolumeContext**](nf-fltkernel-fltdeletevolumecontext.md)

[**FltGetContexts**](nf-fltkernel-fltgetcontexts.md)

[**FltGetFileContext**](nf-fltkernel-fltgetfilecontext.md)

[**FltGetInstanceContext**](nf-fltkernel-fltgetinstancecontext.md)

[**FltGetSectionContext**](nf-fltkernel-fltgetsectioncontext.md)

[**FltGetStreamContext**](nf-fltkernel-fltgetstreamcontext.md)

[**FltGetStreamHandleContext**](nf-fltkernel-fltgetstreamhandlecontext.md)

[**FltGetTransactionContext**](nf-fltkernel-fltgettransactioncontext.md)

[**FltGetVolumeContext**](nf-fltkernel-fltgetvolumecontext.md)

[**FltReferenceContext**](nf-fltkernel-fltreferencecontext.md)

[**FltRegisterFilter**](nf-fltkernel-fltregisterfilter.md)

[**FltReleaseContext**](nf-fltkernel-fltreleasecontext.md)

[**FltSetFileContext**](nf-fltkernel-fltsetfilecontext.md)

[**FltSetInstanceContext**](nf-fltkernel-fltsetinstancecontext.md)

[**FltSetStreamContext**](nf-fltkernel-fltsetstreamcontext.md)

[**FltSetStreamHandleContext**](nf-fltkernel-fltsetstreamhandlecontext.md)

[**FltSetTransactionContext**](nf-fltkernel-fltsettransactioncontext.md)

[**FltSetVolumeContext**](nf-fltkernel-fltsetvolumecontext.md)
