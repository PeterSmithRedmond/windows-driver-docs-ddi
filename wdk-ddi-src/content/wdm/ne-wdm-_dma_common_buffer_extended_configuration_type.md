---
UID: NE:wdm._DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE
title: DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE (wdm.h)
description: Provides the types of optional configurations that can be provided when creating a common buffer from an MDL. The configuration values corresponding to the types are held in the DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION structure.
tech.root: kernel
ms.date: 03/03/2023
keywords: ["DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE enumeration"]
f1_keywords:
 - "wdm/DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE"
 - "DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE"
req.header: wdm.h
req.include-header:
req.target-type: Desktop
req.target-min-winverclnt:
req.target-min-winversvr: Windows Server 2022
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.max-support:
req.typenames: DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE, *PDMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - wdm.h
api_name:
 - DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION_TYPE
targetos: Windows
---

## -description

Provides the types of optional configurations that can be provided when creating a common buffer from an MDL. The configuration values corresponding to the types are held in the [DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION](ns-wdm-dma_common_buffer_extended_configuration.md) structure.

## -enum-fields

### -field CommonBufferConfigTypeLogicalAddressLimits

The associated configuration will contain information about the limits of logical address that can be used to fulfill common buffer creation.

### -field CommonBufferConfigTypeSubSection

The associated configuration will contain information about the subsection within the MDL to use to create the common buffer.

### -field CommonBufferConfigTypeHardwareAccessPermissions

The associated configuration will contain information about the access permissions for the hardware.

### -field CommonBufferConfigTypeMax

The number of common buffer extended configuration values for this enumeration type that represent actual common buffer configuration types.

## -see-also

[DMA_COMMON_BUFFER_EXTENDED_CONFIGURATION](ns-wdm-dma_common_buffer_extended_configuration.md)

[PCREATE_COMMON_BUFFER_FROM_MDL](nc-wdm-pcreate-common-buffer-from-mdl.md)
