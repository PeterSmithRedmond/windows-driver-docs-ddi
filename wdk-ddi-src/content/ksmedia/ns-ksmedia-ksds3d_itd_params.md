---
UID: NS:ksmedia.KSDS3D_ITD_PARAMS
title: KSDS3D_ITD_PARAMS (ksmedia.h)
description: The KSDS3D_ITD_PARAMS structure specifies the parameters applied by the interaural time delay (ITD) algorithm to the left or right channel in a 3D node (KSNODETYPE_3D_EFFECTS).
old-location: audio\ksds3d_itd_params.htm
tech.root: audio
ms.date: 08/03/2021
keywords: ["KSDS3D_ITD_PARAMS structure"]
ms.keywords: "*PKSDS3D_ITD_PARAMS, KSDS3D_ITD_PARAMS, KSDS3D_ITD_PARAMS structure [Audio Devices], PKSDS3D_ITD_PARAMS, PKSDS3D_ITD_PARAMS structure pointer [Audio Devices], aud-prop_169748c9-f538-47d2-ae3c-ae34cca26f00.xml, audio.ksds3d_itd_params, ksmedia/KSDS3D_ITD_PARAMS, ksmedia/PKSDS3D_ITD_PARAMS"
req.header: ksmedia.h
req.include-header: Ksmedia.h
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
req.typenames: KSDS3D_ITD_PARAMS, *PKSDS3D_ITD_PARAMS
f1_keywords:
 - PKSDS3D_ITD_PARAMS
 - ksmedia/PKSDS3D_ITD_PARAMS
 - KSDS3D_ITD_PARAMS
 - ksmedia/KSDS3D_ITD_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - PKSDS3D_ITD_PARAMS
 - KSDS3D_ITD_PARAMS
---

# KSDS3D_ITD_PARAMS structure


## -description

The KSDS3D_ITD_PARAMS structure specifies the parameters applied by the interaural time delay (ITD) algorithm to the left or right channel in a 3D node ([KSNODETYPE_3D_EFFECTS](/windows-hardware/drivers/audio/ksnodetype-3d-effects)).

## -struct-fields

### -field Channel

Specifies the channel number (channel 0 is the left channel; channel 1 is the right channel).

### -field VolSmoothScale

Specifies the ramp factor for scaling volume levels. For more information, see the following Remarks section.

### -field TotalDryAttenuation

Specifies the attenuation factor for the "dry" signal (the original signal before applying a low-pass filter to produce a muffled effect). For more information, see the following Remarks section.

### -field TotalWetAttenuation

Specifies the attenuation factor for the "wet" signal (the muffled signal after the low-pass filter is applied). For more information, see the following Remarks section.

### -field SmoothFrequency

Specifies the sample frequency of the audio stream. When changing to a new **TotalDryAttenuation** or **TotalWetAttenuation** value, the ITD algorithm needs this value to determine the number of samples over which to apply smoothing in order to complete the transition within some fixed time interval. For example, the ITD algorithm implemented by the [KMixer system driver](/windows-hardware/drivers/audio/kernel-mode-wdm-audio-components) uses a transition time interval of roughly 1/8 second.

### -field Delay

Specifies the time delay for this channel. The delay is expressed as an integer number of samples.

## -remarks

This structure is used by the [KSDS3D_ITD_PARAMS_MSG](./ns-ksmedia-ksds3d_itd_params_msg.md) structure, which the [KSPROPERTY_ITD3D_PARAMS](/windows-hardware/drivers/audio/ksproperty-itd3d-params) property request uses to specify the ITD parameters for the left and right channels of a 3D audio stream.

The **Delay** member specifies the amount by which the current channel delays the sound arriving from the source. The interaural time delay is the difference in delays between the two channels.

The attenuated signal is the sum of the attenuated dry signal and the attenuated wet signal:

**TotalDryAttenuation** + **TotalWetAttenuation**

Increasing the size of **TotalWetAttenuation** relative to **TotalDryAttenuation** produces an increasingly muffled sound. The two attenuation factors are calculated from the sound source's position, orientation, and sound cone.

When a KSPROPERTY_ITD3D_PARAMS set-property request changes either **TotalDryAttenuation** or **TotalWetAttenuation**, the change in attenuation level is smoothed over a number of samples in order to avoid generating spurious clicking noises. The **VolSmoothScale** member specifies the amount by which to scale the attenuation of the signal during each step in the smoothing process. This parameter is either a value slightly less than 1 if the attenuation is increasing or slightly greater than 1 if the attenuation is decreasing. At each step in the smoothing process, the attenuation from the previous step is multiplied by this parameter. The process completes when the target attenuation is reached.

## -see-also

[KSDS3D_ITD_PARAMS_MSG](./ns-ksmedia-ksds3d_itd_params_msg.md)

[KSPROPERTY_ITD3D_PARAMS](/windows-hardware/drivers/audio/ksproperty-itd3d-params)

