---
UID: NF:ntddk.IoGetActivityIdIrp
title: IoGetActivityIdIrp function (ntddk.h)
description: The IoGetActivityIdIrp routine retrieves the current activity ID associated with an IRP.
tech.root: kernel
ms.date: 04/20/2023
keywords: ["IoGetActivityIdIrp function"]
ms.keywords: IoGetActivityIdIrp, IoGetActivityIdIrp routine [Kernel-Mode Driver Architecture], kernel.iogetactivityidirp, ntddk/IoGetActivityIdIrp
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 8.
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
req.irql: Any level
targetos: Windows
req.typenames: 
f1_keywords:
 - IoGetActivityIdIrp
 - ntddk/IoGetActivityIdIrp
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - IoGetActivityIdIrp
---

## -description

The IoGetActivityIdIrp routine retrieves the current activity ID associated with an IRP.

## -parameters

### -param Irp [in]

The IRP from which to retrieve the activity ID.

### -param Guid [out]

A pointer to a location  to store the retrieved GUID.

## -returns

IoGetActivityIdIrp returns **STATUS_SUCCESS** if the call is successful. Possible error return values include the following.

| Return code | Description |
|--|--|
| **STATUS_NOT_FOUND** | No activity ID is associated with the request. |
