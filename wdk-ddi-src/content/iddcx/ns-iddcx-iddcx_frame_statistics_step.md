---
UID: NS:iddcx.IDDCX_FRAME_STATISTICS_STEP
title: IDDCX_FRAME_STATISTICS_STEP (iddcx.h)
description: Gives information about the frame processing step being used by the driver.
old-location: display\iddcx_frame_statistics_step.htm
tech.root: display
ms.date: 08/08/2022
keywords: ["IDDCX_FRAME_STATISTICS_STEP structure"]
ms.keywords: IDDCX_FRAME_STATISTICS_STEP, IDDCX_FRAME_STATISTICS_STEP structure, IDDCX_FRAME_STATISTICS_STEP structure [Display Devices], IDDCX_FRAME_STATISTICS_STEP structure pointer [Display Devices], IDDCX_FRAME_STATISTICS_STEP structure structure [Display Devices], display.iddcx_frame_statistics_step, iddcx/IDDCX_FRAME_STATISTICS_STEP
req.header: iddcx.h
req.include-header: 
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
req.typenames: 
f1_keywords:
 - IDDCX_FRAME_STATISTICS_STEP
 - iddcx/IDDCX_FRAME_STATISTICS_STEP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iddcx.h
api_name:
 - IDDCX_FRAME_STATISTICS_STEP
---

# IDDCX_FRAME_STATISTICS_STEP structure

## -description

The **IDDCX_FRAME_STATISTICS_STEP** structure provides information about the frame processing step being used by the driver.

## -struct-fields

### -field Size

Total size of this structure, in bytes.

### -field Type

A [**IDDCX_FRAME_STATISTICS_STEP_TYPE**](ne-iddcx-iddcx_frame_statistics_step_type.md) value that specifies the type of frame processing step.

### -field QpcTime

Specifies the system QPC time of the step.

### -field Data

When driver-defined processing part is used, then the driver can store additional data here.

## -see-also

[**IDDCX_FRAME_STATISTICS**](ns-iddcx-iddcx_frame_statistics.md)
