---
UID: NS:ksmedia.KSPROPERTY_TUNER_INPUT_S
title: KSPROPERTY_TUNER_INPUT_S (ksmedia.h)
description: The KSPROPERTY_TUNER_INPUT_S structure describes the input connection index of a tuner device for devices that support multiple inputs.
old-location: stream\ksproperty_tuner_input_s.htm
tech.root: stream
ms.date: 04/30/2019
keywords: ["KSPROPERTY_TUNER_INPUT_S structure"]
ms.keywords: "*PKSPROPERTY_TUNER_INPUT_S, KSPROPERTY_TUNER_INPUT_S, KSPROPERTY_TUNER_INPUT_S structure [Streaming Media Devices], PKSPROPERTY_TUNER_INPUT_S, PKSPROPERTY_TUNER_INPUT_S structure pointer [Streaming Media Devices], ksmedia/KSPROPERTY_TUNER_INPUT_S, ksmedia/PKSPROPERTY_TUNER_INPUT_S, stream.ksproperty_tuner_input_s, vidcapstruct_db1848a6-76f7-4f65-923e-cfd678a90b64.xml"
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
req.typenames: KSPROPERTY_TUNER_INPUT_S, *PKSPROPERTY_TUNER_INPUT_S
f1_keywords:
 - PKSPROPERTY_TUNER_INPUT_S
 - ksmedia/PKSPROPERTY_TUNER_INPUT_S
 - KSPROPERTY_TUNER_INPUT_S
 - ksmedia/KSPROPERTY_TUNER_INPUT_S
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - PKSPROPERTY_TUNER_INPUT_S
 - KSPROPERTY_TUNER_INPUT_S
---

# KSPROPERTY_TUNER_INPUT_S structure


## -description

The KSPROPERTY_TUNER_INPUT_S structure describes the input connection index of a tuner device for devices that support multiple inputs.

## -struct-fields

### -field Property

Specifies an initialized <a href="/windows-hardware/drivers/stream/ksproperty-structure">KSPROPERTY</a> structure that describes the property set, property ID, and request type.

### -field InputIndex

Specifies the connection index to be used as the tuner input. This value should be in the range of 0 through (number of inputs-1).

## -see-also

<a href="/windows-hardware/drivers/stream/ksproperty-structure">KSPROPERTY</a>



<a href="/windows-hardware/drivers/stream/ksproperty-tuner-input">KSPROPERTY_TUNER_INPUT</a>



<a href="/windows-hardware/drivers/stream/propsetid-tuner">PROPSETID_TUNER</a>

