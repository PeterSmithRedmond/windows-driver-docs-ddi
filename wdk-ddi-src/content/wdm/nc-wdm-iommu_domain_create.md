---
UID: NC:wdm.IOMMU_DOMAIN_CREATE
title: IOMMU_DOMAIN_CREATE (wdm.h)
description: Creates a new DMA remapping device domain (a container for a set of page tables).
tech.root: kernel
ms.date: 01/19/2023
keywords: ["IOMMU_DOMAIN_CREATE callback function"]
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
 - IOMMU_DOMAIN_CREATE
 - wdm/IOMMU_DOMAIN_CREATE
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - wdm.h
api_name:
 - IOMMU_DOMAIN_CREATE
---

## -description

Creates a new DMA remapping device domain (a container for a set of page tables).

## -parameters

### -param OsManagedPageTable [_In_]

A boolean value that indicates whether the page table is managed by the caller or by the HAL.

- TRUE, indicates the HAL owns the page table.

  - Map/Unmap are available.

  - Configure/Flush are unavailable.

- FALSE indicates that the caller owns the page table.

  - Map/Unmap are unavailable.

  - Configure/Flush are available.

### -param DomainOut: [_Out_]

A pointer to IOMMU_DMA_DOMAIN variable that receives an opaque handle used to reference the domain.

## -returns

Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate NTSTATUS values error code. For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

This is deprecated. Consider using [*IOMMU_DOMAIN_CREATE_EX**](nc-wdm-iommu_domain_create_ex.md) and [**DMA_IOMMU_INTERFACE_EX**](ns-wdm-dma_iommu_interface_ex.md).

## -see-also
