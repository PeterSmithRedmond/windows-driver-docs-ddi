---
UID: NC:wdm.PCREATE_COMMON_BUFFER_FROM_MDL
title: PCREATE_COMMON_BUFFER_FROM_MDL (wdm.h)
description: The CreateCommonBufferFromMdl routine will attempt to create a common buffer from an MDL by testing for device access compatibility and potentially mapping the memory to a contiguous logical range depending on the translation type. Like all other common buffer allocation functions, this function does not provide a forward progress guarantee.
ms.date: 05/18/2021
keywords: ["PCREATE_COMMON_BUFFER_FROM_MDL callback function"]
f1_keywords:
 - "wdm/PCREATE_COMMON_BUFFER_FROM_MDL"
 - "PCREATE_COMMON_BUFFER_FROM_MDL"
req.header: wdm.h
req.include-header:
req.target-type: Desktop
req.target-min-winverclnt:
req.target-min-winversvr: Windows Server 2022
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.irql: PASSIVE_LEVEL
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
topic_type:
- apiref
api_type:
- UserDefined
api_location:
- wdm.h
api_name:
- PCREATE_COMMON_BUFFER_FROM_MDL
- CreateCommonBufferFromMdl
targetos: Windows
---

## -description

The CreateCommonBufferFromMdl routine will attempt to create a common buffer from an MDL by testing for device access compatibility and potentially mapping the memory to a contiguous logical range depending on the translation type. Like all other common buffer allocation functions, this function does not provide a forward progress guarantee.

## -parameters

### -param DmaAdapter [in]

Provides a pointer to the DMA Adapter that is performing the operation.

### -param Mdl [in]

Provides the MDL that will be mapped to a common buffer.

For an MDL to be able to back a common buffer, the following conditions must be met:

- The MDL must have pages that are always resident for the lifetime of the common buffer and that are mapped into the system address space. This can be accomplished by the following approaches:

- The MDL is created from a buffer in the non-paged pool via [*MmBuildMdlForNonPagedPool*](nf-wdm-mmbuildmdlfornonpagedpool.md).

- The MDL has been locked via [*MmProbeAndLockPages*](nf-wdm-mmprobeandlockselectedpages.md) and mapped to system space via [*MmGetSystemAddressForMdlSafe*](/windows-hardware/drivers/kernel/mm-bad-pointer#mmgetsystemaddressformdlsafe).

- The physical pages for the MDL have been allocated via [*MmAllocatePagesForMdlEx*](nf-wdm-mmallocatepagesformdl.md) and mapped to system space via [*MmGetSystemAddressForMdlSafe*](/windows-hardware/drivers/kernel/mm-bad-pointer#mmgetsystemaddressformdlsafe).

- The MDL must represent a page-aligned region and be a multiple of PAGE_SIZE.

  - If the SubSection extended configuration is being used, then the portion of the MDL being used must be page-aligned and be a multiple of PAGE_SIZE.

- The MDL must not be a chained MDL.

  - If the SubSection extended configuration is being used, then a chained MDL can be provided, but the portion of the MDL being used must be contained in a single MDL in the chain.

- If DMA Remapping is not being used, the MDL must represent physically contiguous memory and be accessible to the device.

### -param ExtendedConfigs [in]

Provides an optional array of [DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION](ns-wdm-dma_common_buffer_extended_configuration.md) structures to further configure the creation of the MDL backed common buffer.

If multiple configurations of the same [DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE](ne-wdm-_dma_common_buffer_extended_configuration_type.md) are provided in the array, creation will fail.

### -param ExtendedConfigsCount [in]

Provides the number of extended configurations in the *ExtendedConfigs* array.

### -param LogicalAddress [out]

On success provides the logical address of the resulting common buffer.

## -returns

**CreateCommonBufferFromMdl** return **STATUS_SUCCESS** if the call is successful. Possible error return values include the following status codes.

| Return code | Description |
|---|---|
| **STATUS_INVALID_PARAMETER** | The caller has provided an incompatible MDL or extended configuration. |
| **STATUS_NOT_SUPPORTED** | The caller has provided an extended configuration that is not supported on the current system. |
| **STATUS_INSUFFICIENT_RESOURCES** | The system does not have enough memory to create book-keeping and mapping metadata. |

## -remarks

**CreateCommonBufferFromMdl** is not a system routine that can be called directly by name. This routine can be called only by pointer from the address returned in a [*DMA_OPERATIONS*](ns-wdm-_dma_operations.md) structure. Drivers obtain the address of this routine by calling [IoGetDmaAdapter](nf-wdm-iogetdmaadapter.md) with the **Version** member of the *DeviceDescription* parameter set to DEVICE_DESCRIPTION_VERSION3. If **IoGetDmaAdapter** returns **NULL**, the routine is not available on your platform.

A common buffer created by **CreateCommonBufferFromMdl** will be removed via [FreeCommonBuffer](nc-wdm-pfree_common_buffer.md). The caller must provide the system virtual address as the virtual address to ensure the common buffer is correctly removed from the Adapter's common buffer bookkeeping structures. The driver is still responsible for unlocking and freeing the MDL and its backing pages.

To create a common buffer where the HAL is responsible for maintaining the backing memory, use [AllocateCommonBufferWithBounds](nc-wdm-pallocate_common_buffer_with_bounds.md).

## -see-also

[**DMA_ADAPTER**](ns-wdm-_dma_adapter.md)

[**DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION**](ns-wdm-dma_common_buffer_extended_configuration.md)

[DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE](ne-wdm-_dma_common_buffer_extended_configuration_type.md)

[**DMA_OPERATIONS**](ns-wdm-_dma_operations.md)

[FreeCommonBuffer](nc-wdm-pfree_common_buffer.md)

[IoGetDmaAdapter](nf-wdm-iogetdmaadapter.md)

[PALLOCATE_COMMON_BUFFER_WITH_BOUNDS](nc-wdm-pallocate_common_buffer_with_bounds.md)
