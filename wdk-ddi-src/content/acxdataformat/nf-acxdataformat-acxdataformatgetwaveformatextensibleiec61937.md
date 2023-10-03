---
UID: NF:acxdataformat.AcxDataFormatGetWaveFormatExtensibleIec61937
tech.root: audio
title: AcxDataFormatGetWaveFormatExtensibleIec61937
ms.date: 12/15/2022
targetos: Windows
description: The AcxDataFormatGetWaveFormatExtensibleIec61937 function gets the WAVEFORMATEXTENSIBLE_IEC61937 structure associated with the specified data format.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxdataformat.h
req.idl: 
req.include-header: 
req.irql: <= DISPATCH_LEVEL
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - acxdataformat.h
api_name:
 - AcxDataFormatGetWaveFormatExtensibleIec61937
f1_keywords:
 - AcxDataFormatGetWaveFormatExtensibleIec61937
 - acxdataformat/AcxDataFormatGetWaveFormatExtensibleIec61937
dev_langs:
 - c++
---

## -description

The **AcxDataFormatGetWaveFormatExtensibleIec61937** function gets the WAVEFORMATEXTENSIBLE_IEC61937 structure associated with the specified data format.

## -parameters

### -param DataFormat [in]

The data format for which to retrieve the WAVEFORMATEXTENSIBLE_IEC61937 structure.

## -returns

Returns a pointer to the WAVEFORMATEXTENSIBLE_IEC61937 structure associated with the specified *DataFormat*.

## -remarks

### ACX requirements

**Minimum ACX version:** 1.0

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [Representing Formats for IEC 61937 Transmissions](/windows/win32/coreaudio/representing-formats-for-iec-61937-transmissions)
- [acxdataformat.h header](index.md)
