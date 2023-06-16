---
UID: NI:d3dukmdt.IOCTL_GPUP_DRIVER_ESCAPE
title: IOCTL_GPUP_DRIVER_ESCAPE (d3dukmdt.h)
description: The user mode emulation DLL calls this IOCTL to exchange information with the kernel mode driver.
ms.date: 10/19/2018
keywords: ["IOCTL_GPUP_DRIVER_ESCAPE IOCTL"]
req.header: d3dukmdt.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.max-support: 
targetos: Windows
ms.custom: RS5
tech.root: display
f1_keywords:
 - IOCTL_GPUP_DRIVER_ESCAPE
 - d3dukmdt/IOCTL_GPUP_DRIVER_ESCAPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3dukmdt.h
api_name:
 - IOCTL_GPUP_DRIVER_ESCAPE
dev_langs:
 - c++
---

# IOCTL_GPUP_DRIVER_ESCAPE IOCTL

### Major Code:  [IRP_MJ_DEVICE_CONTROL](/windows-hardware/drivers/kernel/irp-mj-device-control)


## -description

The user mode emulation DLL calls this IOCTL to exchange information with the kernel mode driver.

## -ioctlparameters

### -ioctl-major-code

### -input-buffer


### -input-buffer-length 


### -output-buffer


### -output-buffer-length 


### -in-out-buffer


### -inout-buffer-length 


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.
Otherwise, Status to the appropriate error condition as a NTSTATUS code. 
For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

## -see-also
