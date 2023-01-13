---
UID: NF:ntddk.PsDetachSiloFromCurrentThread
title: PsDetachSiloFromCurrentThread function (ntddk.h)
description: This routine removes a thread from a silo which was added by an attach. For more info about attaching, see the PsAttachSiloToCurrentThread routine.
tech.root: kernel
ms.date: 12/07/2022
keywords: ["PsDetachSiloFromCurrentThread function"]
ms.keywords: PsDetachSiloFromCurrentThread, PsDetachSiloFromCurrentThread routine [Kernel-Mode Driver Architecture], kernel.psdetachsilofromcurrentthread, ntddk/PsDetachSiloFromCurrentThread
req.header: ntddk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607
req.target-min-winversvr: Windows Server 2016
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
req.typenames: 
f1_keywords:
 - PsDetachSiloFromCurrentThread
 - ntddk/PsDetachSiloFromCurrentThread
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddk.h
api_name:
 - PsDetachSiloFromCurrentThread
---

## -description

This routine removes a thread from a silo which was added by an attach. For more info about attaching, see the  [PsAttachSiloToCurrentThread](./nf-ntddk-psattachsilotocurrentthread.md) routine.

The caller is responsible for dereferencing the object after the detach has completed.

## -parameters

### -param PreviousSilo [in]

The value returned from the silo attach call.

## -see-also

[PsAttachSiloToCurrentThread](./nf-ntddk-psattachsilotocurrentthread.md)