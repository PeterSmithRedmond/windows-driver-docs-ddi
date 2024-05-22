---
UID: NS:d3d12umddi.D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095
tech.root: display
title: D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095
ms.date: 05/14/2024
targetos: Windows
description: Learn more about the D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095 structure.
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
req.target-min-winverclnt: Windows 11, version 24H2 (WDDM 3.2)
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12umddi.h
api_name:
 - D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095
f1_keywords:
 - D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095
 - d3d12umddi/D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095
---

## -description

The **D3D12DDI_VIDEO_ENCODER_CODEC_AV1_LOOP_FILTER_DELTA_CONFIG_0095** structure contains configuration information related to the loop filter delta settings within an AV1 video encoder.

## -struct-fields

### -field DeltaLFPresent

Related to AV1 syntax delta_lf_params(). Requires that [**D3D12DDI_VIDEO_ENCODER_AV1_FEATURE_0095_FLAG_DELTA_LF_PARAMS**](ne-d3d12umddi-d3d12ddi_video_encoder_av1_feature_0095_flags.md) be supported/enabled.

### -field DeltaLFMulti

Related to AV1 syntax delta_lf_params().

### -field DeltaLFRes

Related to AV1 syntax delta_lf_params().

## -remarks

This structure is related to AV1 syntax delta_lf_params().

See [D3D12 AV1 video encoding](/windows-hardware/drivers/display/video-encoding-d3d12-av1.md) for more information.

## -see-also

[**D3D12DDI_VIDEO_ENCODER_AV1_FEATURE_0095_FLAGS**](ne-d3d12umddi-d3d12ddi_video_encoder_av1_feature_0095_flags.md)

[**D3D12DDI_VIDEO_ENCODER_AV1_PICTURE_CONTROL_CODEC_DATA_0095**](ns-d3d12umddi-d3d12ddi_video_encoder_av1_picture_control_codec_data_0095.md)

[**D3D12DDI_VIDEO_ENCODER_AV1_POST_ENCODE_VALUES_0095**](ns-d3d12umddi-d3d12ddi_video_encoder_av1_post_encode_values_0095.md)
