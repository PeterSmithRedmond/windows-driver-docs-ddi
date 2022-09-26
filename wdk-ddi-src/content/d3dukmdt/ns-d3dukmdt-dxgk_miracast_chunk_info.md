---
UID: NS:d3dukmdt.__unnamed_struct_18
title: DXGK_MIRACAST_CHUNK_INFO (d3dukmdt.h)
description: The DXGK_MIRACAST_CHUNK_INFO structure contains information about a specified wireless display (Miracast) encode chunk.
tech.root: display
ms.date: 09/26/2022
keywords: ["DXGK_MIRACAST_CHUNK_INFO structure"]
ms.keywords: DXGK_MIRACAST_CHUNK_INFO, DXGK_MIRACAST_CHUNK_INFO structure [Display Devices], d3dukmdt/DXGK_MIRACAST_CHUNK_INFO, display.dxgk_miracast_chunk_info
req.header: d3dukmdt.h
req.include-header: D3dukmdt.h, D3dkmddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: DXGK_MIRACAST_CHUNK_INFO
f1_keywords:
 - DXGK_MIRACAST_CHUNK_INFO
 - d3dukmdt/DXGK_MIRACAST_CHUNK_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3dukmdt.h
api_name:
 - DXGK_MIRACAST_CHUNK_INFO
---

## -description

Contains info about a specified wireless display (Miracast) encode chunk.

## -struct-fields

### -field ChunkType

The type of chunk that is to be processed, specified as a [DXGK_MIRACAST_CHUNK_TYPE](/windows-hardware/drivers/ddi/d3dukmdt/ne-d3dukmdt-_dxgk_miracast_chunk_type) enumeration value.

### -field ChunkId

The identifier for this chunk, of type [**DXGK_MIRACAST_CHUNK_ID**](/windows-hardware/drivers/ddi/d3dukmdt/ns-d3dukmdt-dxgk_miracast_chunk_id).

### -field ProcessingTime

The time, in microseconds, that it took to process this chunk.

### -field EncodeRate

The encode bit rate, in kilobits per second, that the display miniport driver reported for this chunk.

## -see-also

[**DXGK_MIRACAST_CHUNK_ID**](/windows-hardware/drivers/ddi/d3dukmdt/ns-d3dukmdt-dxgk_miracast_chunk_id)

[DXGK_MIRACAST_CHUNK_TYPE](/windows-hardware/drivers/ddi/d3dukmdt/ne-d3dukmdt-_dxgk_miracast_chunk_type)
