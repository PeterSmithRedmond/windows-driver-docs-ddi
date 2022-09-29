---
UID: NC:d3d12umddi.PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075
title: PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075 (d3d12umddi.h)
description: The PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075 callback function checks resource allocation information.
ms.date: 09/29/2022
keywords: ["PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075 callback function"]
ms.keywords: PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075, PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075 callback, d3d12umddi/pfnCheckResourceAllocationInfo, display.pfnd3d12ddi_checkresourceallocationinfo_0075, pfnCheckResourceAllocationInfo, pfnCheckResourceAllocationInfo callback function [Display Devices]
req.header: d3d12umddi.h
req.include-header: D3d12umddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
tech.root: display
req.typenames: 
f1_keywords:
 - PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075
 - d3d12umddi/PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - D3d12umddi.h
api_name:
 - PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075
---

# PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075 callback function

## -description

The **PFND3D12DDI_CHECKRESOURCEALLOCATIONINFO_0075** callback function supports checking resource allocation information.

## -parameters

### -param unnamedParam1

A handle to the display device (graphics context).

### -param unnamedParam2 [in]

Pointer to a [**D3D12DDIARG_CREATERESOURCE_0075**](ns-d3d12umddi-d3d12ddiarg_createresource_0075.md) structure.

### -param unnamedParam3

Resource optimization flags.

### -param AlignmentRestriction

A resource alignment restriction value.

### -param VisibleNodeMask

For a multi-adapter operation, this value indicates the set of nodes where the resource is visible. Passing zero is equivalent to passing one, in order to simplify the usage of single-GPU adapters.

### -param unnamedParam6 [out]

Pointer to a [**D3D12DDI_RESOURCE_ALLOCATION_INFO_0022**](ns-d3d12umddi-d3d12ddi_resource_allocation_info_0022.md) structure containing information for resource allocation.

## -remarks

This callback function is part of a two step process of resource creation. This function determines the sizes and alignments of the resource data, additional data header, and additional data is determined, along with the texture layout. When the resource description is passed into this function, the layout of the resource description may be set to _UNDEFINED. This allows the driver to choose any texture layout. When the layout of the resource description is **STANDARD_SWIZZLE** or **ROW_MAJOR**, the driver must return out the corresponding value as its choice.

This callback function is accessed by using the [**D3D12DDI_DEVICE_FUNCS_CORE_0075**](ns-d3d12umddi-d3d12ddi_device_funcs_core_0075.md) structure.

## -see-also

[**D3D12DDI_DEVICE_FUNCS_CORE_0075**](ns-d3d12umddi-d3d12ddi_device_funcs_core_0075.md)

[**D3D12DDI_RESOURCE_ALLOCATION_INFO_0022**](ns-d3d12umddi-d3d12ddi_resource_allocation_info_0022.md)

[**D3D12DDIARG_CREATERESOURCE_0075**](ns-d3d12umddi-d3d12ddiarg_createresource_0075.md)
