---
UID: NE:d3d12umddi.D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080
tech.root: display
title: D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080
ms.date: 05/20/2024
targetos: Windows
description: Learn more about the D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080 enumeration.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12umddi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 (WDDM 3.0)
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12umddi.h
api_name:
 - D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080
f1_keywords:
 - D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080
 - d3d12umddi/D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080
---

## -description

The **D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAGS_0080** enumeration specifies flags for the H.264-specific picture control properties.

## -enum-fields

### -field D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAG_0080_NONE

No flags.

### -field D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAG_0080_REQUEST_INTRA_CONSTRAINED_SLICES

Requests slice-constrained encoding for this frame, in which every slice in a frame is encoded independently from other slices in the same frame. Check [**D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264_FLAG_0080_INTRA_SLICE_CONSTRAINED_ENCODING_SUPPORT**](ne-d3d12umddi-d3d12ddi_video_encoder_codec_configuration_support_h264_flags_0080.md) for support. This mode restricts the motion vector search range to the region box of the current slice; that is, motion vectors cannot be used outside the slice boundary.

### -field D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_FLAG_0099_0_REQUEST_NUM_REF_IDX_ACTIVE_OVERRIDE_FLAG_SLICE

Requests an override of the number of active reference indices for slice encoding. Added in Windows 11, version 24H2 (WDDM 3.2).

## -remarks

See [D3D12 video encoding](/windows-hardware/drivers/display/video-encoding-d3d12) for general information.

## -see-also

[**D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264_FLAGS_0080**](ne-d3d12umddi-d3d12ddi_video_encoder_codec_configuration_support_h264_flags_0080.md)

[**D3D12DDI_VIDEO_ENCODER_PICTURE_CONTROL_CODEC_DATA_H264_0082_0**](ns-d3d12umddi-d3d12ddi_video_encoder_picture_control_codec_data_h264_0082_0.md)
