---
UID: NS:d3d12umddi.D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0
tech.root: display
title: D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0
ms.date: 05/20/2024
targetos: Windows
description: Learn more about D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12umddi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 (WDDM 3.0)
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12umddi.h
api_name:
 - D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0
f1_keywords:
 - D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0
 - d3d12umddi/D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0
dev_langs:
 - c++
---

## -description

The **D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_0082_0** structure contains configuration information for a video codec.

## -struct-fields

### -field DataSize

Size of the referenced data, in bytes.

### -field pH264Config

Pointer to a [**D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_H264_0082_0**](ns-d3d12umddi-d3d12ddi_video_encoder_codec_configuration_h264_0082_0.md) structure that contains H.264 codec configuration information.

### -field pHEVCConfig

Pointer to a [**D3D12DDI_VIDEO_ENCODER_CODEC_CONFIGURATION_HEVC_0082_0**](ns-d3d12umddi-d3d12ddi_video_encoder_codec_configuration_hevc_0082_0.md) structure that contains HEVC codec configuration information.

### -field pAV1Config

Pointer to a [**D3D12DDI_VIDEO_ENCODER_AV1_CODEC_CONFIGURATION_0095**](ns-d3d12umddi-d3d12ddi_video_encoder_av1_codec_configuration_0095.md) structure that contains AV1 codec configuration information. Added in Windows 11, version 24H2 (WDDM 3.2).

## -remarks

See [D3D12 video encoding](/windows-hardware/drivers/display/video-encoding-d3d12) for general information.

## -see-also

[**D3D12DDIARG_CREATE_VIDEO_ENCODER_0082_0**](ns-d3d12umddi-d3d12ddiarg_create_video_encoder_0082_0.md)

[**D3D12DDICAPS_VIDEO_ENCODER_SUPPORT_DATA_0083_0**](ns-d3d12umddi-d3d12ddicaps_video_encoder_support_data_0083_0.md)
