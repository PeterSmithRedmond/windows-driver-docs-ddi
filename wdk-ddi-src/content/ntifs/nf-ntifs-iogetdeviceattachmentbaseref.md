---
UID: NF:ntifs.IoGetDeviceAttachmentBaseRef
title: IoGetDeviceAttachmentBaseRef function (ntifs.h)
description: The IoGetDeviceAttachmentBaseRef routine returns a pointer to the lowest-level device object in a file system or device driver stack.
old-location: ifsk\iogetdeviceattachmentbaseref.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["IoGetDeviceAttachmentBaseRef function"]
ms.keywords: IoGetDeviceAttachmentBaseRef, IoGetDeviceAttachmentBaseRef routine [Installable File System Drivers], ifsk.iogetdeviceattachmentbaseref, ioref_ab9c898e-74be-48aa-9462-d78d0e34c435.xml, ntifs/IoGetDeviceAttachmentBaseRef
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Windows 2000 SP4 Update Rollup; Windows XP
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
 - IoGetDeviceAttachmentBaseRef
 - ntifs/IoGetDeviceAttachmentBaseRef
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - IoGetDeviceAttachmentBaseRef
---

# IoGetDeviceAttachmentBaseRef function


## -description

The <b>IoGetDeviceAttachmentBaseRef</b> routine returns a pointer to the lowest-level device object in a file system or device driver stack.

## -parameters

### -param DeviceObject [in]


A pointer to a device object in the stack.

## -returns

<b>IoGetDeviceAttachmentBaseRef</b> returns a pointer to the device object at the bottom of the file system or device driver stack. If the given device object is not attached to a driver stack, <b>IoGetDeviceAttachmentBaseRef</b> returns  the device object pointer in <i>DeviceObject</i>.

## -remarks

A file system filter driver typically calls <b>IoGetDeviceAttachmentBaseRef</b> to get the lowest-level device object in a file system driver stack. Often this is done when the filter driver receives notification that a file system has registered or unregistered itself as an active file system. The filter driver's notification callback routine calls <b>IoGetDeviceAttachmentBaseRef</b> to get a pointer to the file system's control device object, and then calls <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-obquerynamestring">ObQueryNameString</a> to retrieve this object's name for debugging purposes. 

<b>IoGetDeviceAttachmentBaseRef</b> increments the reference count on the device object at the bottom of the stack. Thus every successful call to <b>IoGetDeviceAttachmentBaseRef</b> must be matched by a subsequent call to <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-obdereferenceobject">ObDereferenceObject</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ioenumeratedeviceobjectlist">IoEnumerateDeviceObjectList</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-iogetlowerdeviceobject">IoGetLowerDeviceObject</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ioregisterfsregistrationchange">IoRegisterFsRegistrationChange</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-iounregisterfsregistrationchange">IoUnregisterFsRegistrationChange</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-obdereferenceobject">ObDereferenceObject</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-obquerynamestring">ObQueryNameString</a>
