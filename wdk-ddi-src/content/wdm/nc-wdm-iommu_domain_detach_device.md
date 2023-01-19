---
UID: NC:wdm.IOMMU_DOMAIN_DETACH_DEVICE
title: IOMMU_DOMAIN_DETACH_DEVICE (wdm.h)
description: Detaches a device from an existing domain.
tech.root: kernel
ms.date: 01/19/2023
keywords: ["IOMMU_DOMAIN_DETACH_DEVICE callback function"]
req.header: wdm.h
req.include-header: Wdm.h
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
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
f1_keywords:
 - IOMMU_DOMAIN_DETACH_DEVICE
 - wdm/IOMMU_DOMAIN_DETACH_DEVICE
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - wdm.h
api_name:
 - IOMMU_DOMAIN_DETACH_DEVICE
---

## -description

Detaches a device from an existing domain.

## -parameters

### -param Domain [_In_]

A pointer to the handle to the domain.

### -param PhysicalDeviceObject [_In_]

A pointer the physical device object (PDO) in the device stack of the device.

### -param InputMappingId [_In_]

The input mapping for the device's desired stream.

## -returns

Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate NTSTATUS Values error code. For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

It is driver's responsibility to ensure that this function is not called concurrently with IOMMU_DOMAIN_ATTACH_DEVICE or IOMMU_SET_DEVICE_FAULT_REPORTING calls on the same device.

InputMappingId is used only for ACPI-enumerated devices on ARM64. For all other cases, this value must be zero.

If multiple devices are simultaneously attached using the _MappingCount_ value specified in the [_IOMMU_DOMAIN_ATTACH_DEVICE_](nc-wdm-iommu_domain_attach_device.md) call, then those devices can only be detached as a group by specifying an _InputMappingId_ value that is equal to the _InputMappingIdBase_ value of [_IOMMU_DOMAIN_ATTACH_DEVICE_] used when attaching.

This is deprecated. Consider using [**IOMMU_DOMAIN_DETACH_DEVICE_EX**](nc-wdm-iommu_domain_detach_device_ex.md) and [**DMA_IOMMU_INTERFACE_EX**](ns-wdm-dma_iommu_interface_ex.md).

## -see-also
