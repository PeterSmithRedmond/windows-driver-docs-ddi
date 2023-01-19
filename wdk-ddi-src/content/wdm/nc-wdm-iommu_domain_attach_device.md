---
UID: NC:wdm.IOMMU_DOMAIN_ATTACH_DEVICE
title: IOMMU_DOMAIN_ATTACH_DEVICE (wdm.h)
description: Attaches a device to an existing domain.
tech.root: kernel
ms.date: 01/19/2023
keywords: ["IOMMU_DOMAIN_ATTACH_DEVICE callback function"]
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
 - IOMMU_DOMAIN_ATTACH_DEVICE
 - wdm/IOMMU_DOMAIN_ATTACH_DEVICE
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - wdm.h
api_name:
 - IOMMU_DOMAIN_ATTACH_DEVICE
---

## -description

Attaches a device to an existing domain.

## -parameters

### -param Domain [_In_]

A pointer to the handle to the domain.

### -param PhysicalDeviceObject [_In_]

A pointer the physical device object (PDO) in the device stack of the device.

### -param InputMappingIdBase [_In_]

The input mapping base for the device's desired stream.

### -param MappingCount [_In_]

The count of mappings beginning at the base.

## -returns

Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate NTSTATUS values error code. For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

It is driver's responsibility to ensure that this function is not called concurrently with IOMMU_DOMAIN_DETACH_DEVICE or IOMMU_SET_DEVICE_FAULT_REPORTING calls on the same device.

_InputMappingIdBase_ and _MappingCount_ are intended only to accommodate ACPI-enumerated devices that support multiple stream IDs on ARM64. For any other device or architecture, these values must be:

- InputMappingIdBase = 0

- MappingCount = 1

This is deprecated. Consider using [**IOMMU_DOMAIN_ATTACH_DEVICE_EX**](nc-wdm-iommu_domain_attach_device_ex.md) and [**DMA_IOMMU_INTERFACE_EX**](ns-wdm-dma_iommu_interface_ex.md).

## -see-also
