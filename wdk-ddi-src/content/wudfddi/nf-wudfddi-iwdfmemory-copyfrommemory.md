---
UID: NF:wudfddi.IWDFMemory.CopyFromMemory
title: IWDFMemory::CopyFromMemory (wudfddi.h)
description: The CopyFromMemory method safely copies data from the specified source buffer and prevents overruns that the copy operation might otherwise cause.
old-location: wdf\iwdfmemory_copyfrommemory.htm
tech.root: wdf
ms.date: 08/12/2022
keywords: ["IWDFMemory::CopyFromMemory"]
ms.keywords: CopyFromMemory, CopyFromMemory method, CopyFromMemory method,IWDFMemory interface, IWDFMemory interface,CopyFromMemory method, IWDFMemory.CopyFromMemory, IWDFMemory::CopyFromMemory, UMDFMemoryObjectRef_c5bc961a-62e9-4692-bbd7-6551b268b08b.xml, umdf.iwdfmemory_copyfrommemory, wdf.iwdfmemory_copyfrommemory, wudfddi/IWDFMemory::CopyFromMemory
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IWDFMemory::CopyFromMemory
 - wudfddi/IWDFMemory::CopyFromMemory
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WUDFx.dll
api_name:
 - IWDFMemory::CopyFromMemory
---

# IWDFMemory::CopyFromMemory

## -description

> [!WARNING]
> UMDF 2 is the latest version of UMDF and supersedes UMDF 1. All new UMDF drivers should be written using UMDF 2. No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10. Universal Windows drivers must use UMDF 2. For more info, see [Getting Started with UMDF](/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2).

The **CopyFromMemory** method safely copies data from the specified source buffer and prevents overruns that the copy operation might otherwise cause.

## -parameters

### -param Source [in]

A pointer to the [IWDFMemory](./nn-wudfddi-iwdfmemory.md) interface for the memory object that is the source of the copy operation.

### -param SourceOffset [in, optional]

A pointer to a [WDFMEMORY_OFFSET](../wudfddi_types/ns-wudfddi_types-_wdfmemory_offset.md) structure that describes the information that is copied from a memory block. This parameter is optional. The driver can pass **NULL** if the entire source buffer is copied.

The **BufferOffset** member of the WDFMEMORY_OFFSET structure, if not **NULL**, indicates the offset into the source buffer to start the copy operation from.

The **BufferLength** member should be set to 0; the framework ignores this member because the amount of data that is copied depends on the length and offset combination of the current destination buffer.

## -returns

**CopyFromMemory** returns S_OK if the operation succeeds. Otherwise, this method returns one of the error codes that are defined in Winerror.h.

## -see-also

- [IWDFMemory](./nn-wudfddi-iwdfmemory.md)
- [WDFMEMORY_OFFSET](../wudfddi_types/ns-wudfddi_types-_wdfmemory_offset.md)
