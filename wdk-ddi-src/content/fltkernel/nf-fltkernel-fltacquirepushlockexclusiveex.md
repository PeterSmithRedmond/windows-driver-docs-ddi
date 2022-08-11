---
UID: NF:fltkernel.FltAcquirePushLockExclusiveEx
title: FltAcquirePushLockExclusiveEx function (fltkernel.h)
description: The FltAcquirePushLockExclusiveEx routine acquires the given push lock for exclusive access by the calling thread.
ms.date: 08/11/2022
tech.root: ifsk
keywords: ["FltAcquirePushLockExclusiveEx function"]
ms.keywords: FltAcquirePushLockExclusiveEx
req.header: fltkernel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: FltMgr.lib
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: RS5
f1_keywords:
 - FltAcquirePushLockExclusiveEx
 - fltkernel/FltAcquirePushLockExclusiveEx
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - fltmgr.lib
 - fltmgr.sys
api_name:
 - FltAcquirePushLockExclusiveEx
dev_langs:
 - c++
---

# FltAcquirePushLockExclusiveEx function

## -description

The **FltAcquirePushLockExclusiveEx** routine acquires the given push lock for exclusive access by the calling thread.

## -parameters

### -param PushLock [in, out]

Opaque push lock pointer. This pointer must have been initialized by a previous call to [**FltInitializePushLock**](nf-fltkernel-fltinitializepushlock.md).

### -param Flags

A bitmask of flags that control the attributes of the lock. **Flags** can be the following value.

| Flag | Meaning |
| ---- | ------- |
| FLT_PUSH_LOCK_DISABLE_AUTO_BOOST | Disable push lock auto boost. |
| FLT_PUSH_LOCK_ENABLE_AUTO_BOOST  | Deprecated; has no effect. Enables push lock auto boost. |

## -returns

None.

## -remarks

**FltAcquirePushLockExclusiveEx** acquires the given push lock for exclusive access by the calling thread.

Push locks are similar to ERESOURCE structures (also called resources) in that they can be acquired for shared or exclusive access. For more information about push locks, see the reference entry for [**FltInitializePushLock**](nf-fltkernel-fltinitializepushlock.md).

Unlike ERESOURCE structures, push locks cannot be acquired recursively. If the caller already has acquired the push lock for exclusive or shared access, the thread will hang.

When the caller will be given exclusive access to the given push lock depends on the following:

* If the push lock is currently unowned, exclusive access is granted immediately to the current thread.

* If the push lock has already been acquired for exclusive or shared access by another thread, the current thread is put into a wait state until the push lock can be acquired.

## -see-also

[**FltInitializePushLock**](nf-fltkernel-fltinitializepushlock.md)
