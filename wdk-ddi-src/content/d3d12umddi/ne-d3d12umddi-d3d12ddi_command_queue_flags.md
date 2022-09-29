---
UID: NE:d3d12umddi.D3D12DDI_COMMAND_QUEUE_FLAGS
title: D3D12DDI_COMMAND_QUEUE_FLAGS (d3d12umddi.h)
description: Contains values for the video command queue.
old-location: display\d3d12ddi_command_queue_flags.htm
ms.date: 09/22/2022
keywords: ["D3D12DDI_COMMAND_QUEUE_FLAGS enumeration"]
ms.keywords: D3D12DDI_COMMAND_QUEUE_FLAGS, D3D12DDI_COMMAND_QUEUE_FLAGS enumeration [Display Devices], D3D12DDI_COMMAND_QUEUE_FLAG_0022_VIDEO_DECODE, D3D12DDI_COMMAND_QUEUE_FLAG_0022_VIDEO_PROCESS, D3D12DDI_COMMAND_QUEUE_FLAG_3D, D3D12DDI_COMMAND_QUEUE_FLAG_COMPUTE, D3D12DDI_COMMAND_QUEUE_FLAG_COPY, D3D12DDI_COMMAND_QUEUE_FLAG_NONE, D3D12DDI_COMMAND_QUEUE_FLAG_PAGING, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAGS, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAG_0022_VIDEO_DECODE, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAG_0022_VIDEO_PROCESS, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAG_3D, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAG_COMPUTE, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAG_COPY, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAG_NONE, d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAG_PAGING, display.d3d12ddi_command_queue_flags
req.header: d3d12umddi.h
req.include-header: D3d12umddi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: D3D12DDI_COMMAND_QUEUE_FLAGS
f1_keywords:
 - D3D12DDI_COMMAND_QUEUE_FLAGS
 - d3d12umddi/D3D12DDI_COMMAND_QUEUE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3d12umddi.h
api_name:
 - D3D12DDI_COMMAND_QUEUE_FLAGS
---

# D3D12DDI_COMMAND_QUEUE_FLAGS enumeration

## -description

The **D3D12DDI_COMMAND_QUEUE_FLAGS** enumeration contains values for the command queue.

## -enum-fields

### -field D3D12DDI_COMMAND_QUEUE_FLAG_NONE:0x00000000

No flags.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_3D:0x00000001

3D.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_COMPUTE:0x00000002

Compute.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_COPY:0x00000004

Copy.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_PAGING:0x00000008

Paging.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_0020_VIDEO_LEGACY:0x00000010

Deprecated; do not use.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_0022_VIDEO_DECODE:0x00000010

Decode video.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_0022_VIDEO_PROCESS:0x00000020

Process video.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_0053_VIDEO_ENCODE:0x00000040

Video encode.

### -field D3D12DDI_COMMAND_QUEUE_FLAG_IMAGE:0x00000080

Reserved; do not use.

## -remarks

There are separate queue types for video decode and video processing.  The video decode command queue only supports submitting video decode command lists and the video process command queue only supports submitting video process command lists.  Both video decode and video process share the same DDI table definition, but separate table instances are retrieved from the driver for each type, see [**D3D12DDI_TABLE_TYPE**](ne-d3d12umddi-d3d12ddi_table_type.md).

Because video decode and video processing are separate queue types, they are necessarily separate queue instances. Applications are required to synchronize between separate queue instances; therefore, drivers must not implicitly synchronize between decode and video process queues.

## -see-also

[**D3D12DDI_D3D12_OPTIONS_DATA_0089**](ns-d3d12umddi-d3d12ddi_d3d12_options_data_0089.md)
