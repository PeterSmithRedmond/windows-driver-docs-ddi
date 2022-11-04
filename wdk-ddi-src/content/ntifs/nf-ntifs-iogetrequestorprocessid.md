---
UID: NF:ntifs.IoGetRequestorProcessId
title: IoGetRequestorProcessId function (ntifs.h)
description: The IoGetRequestorProcessId routine returns the unique 32-bit process ID for the thread that originally requested a given I/O operation.
old-location: ifsk\iogetrequestorprocessid.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["IoGetRequestorProcessId function"]
ms.keywords: IoGetRequestorProcessId, IoGetRequestorProcessId routine [Installable File System Drivers], ifsk.iogetrequestorprocessid, ioref_a08b37d7-b999-4e40-a0aa-c62744fee6dd.xml, ntifs/IoGetRequestorProcessId
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Windows 2000
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <= DISPATCH_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - IoGetRequestorProcessId
 - ntifs/IoGetRequestorProcessId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - IoGetRequestorProcessId
---

# IoGetRequestorProcessId function


## -description

The <b>IoGetRequestorProcessId</b> routine returns the unique 32-bit process ID for the thread that originally requested a given I/O operation.

## -parameters

### -param Irp [in]


A pointer to the I/O request packet (IRP) for the specified I/O operation.

## -returns

<b>IoGetRequestorProcessId</b> returns the process ID for the thread that requested the I/O operation. If the IRP is not associated with any thread, <b>IoGetRequestorProcessId</b> returns zero.

## -remarks

On Microsoft Windows XP and later, <b>IoGetRequestorProcessId</b> returns the process ID for the process to which the thread is currently attached. 

On Microsoft Windows 2000 and earlier, <b>IoGetRequestorProcessId</b> returns the process ID for the process that created the thread. 

For more information about using system threads and managing synchronization within a nonarbitrary thread context, see <a href="/windows-hardware/drivers/ddi/_kernel/#driver-threads-dispatcher-objects-and-resources">Driver Threads, Dispatcher Objects, and Resources</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-iogetrequestorprocess">IoGetRequestorProcess</a>
