---
UID: NC:d3dkmthk.PFND3DKMT_CHECKMONITORPOWERSTATE
title: PFND3DKMT_CHECKMONITORPOWERSTATE (d3dkmthk.h)
description: The PFND3DKMT_CHECKMONITORPOWERSTATE function verifies the power state of a monitor. The function returns STATUS_SUCCESS on successful verification.
old-location: display\d3dkmtcheckmonitorpowerstate.htm
ms.date: 05/10/2018
keywords: ["PFND3DKMT_CHECKMONITORPOWERSTATE callback function"]
ms.keywords: D3DKMTCheckMonitorPowerState, D3DKMTCheckMonitorPowerState callback function [Display Devices], OpenGL_Functions_d05a2b63-fe81-45f0-908d-94043416b1d0.xml, PFND3DKMT_CHECKMONITORPOWERSTATE, PFND3DKMT_CHECKMONITORPOWERSTATE callback, d3dkmthk/D3DKMTCheckMonitorPowerState, display.d3dkmtcheckmonitorpowerstate
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Universal
req.target-min-winverclnt: Windows Vista
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
 - PFND3DKMT_CHECKMONITORPOWERSTATE
 - d3dkmthk/PFND3DKMT_CHECKMONITORPOWERSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - d3dkmthk.h
api_name:
 - PFND3DKMT_CHECKMONITORPOWERSTATE
---

# PFND3DKMT_CHECKMONITORPOWERSTATE callback function


## -description

The <b>D3DKMTCheckMonitorPowerState</b> function verifies the power state of a monitor.

## -parameters

### -param unnamedParam1

*pData* [in]

A pointer to a <a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_checkmonitorpowerstate">D3DKMT_CHECKMONITORPOWERSTATE</a> structure that describes the connection to the monitor for which to check the power state.

## -returns

<b>D3DKMTCheckMonitorPowerState</b> returns one of the following values:

|Return code|Description|
|--- |--- |
|STATUS_SUCCESS|The power state of the monitor was successfully verified.|
|STATUS_INVALID_PARAMETER|Parameters were validated and determined to be incorrect.|

This function might also return other <b>NTSTATUS</b> values.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmthk/ns-d3dkmthk-_d3dkmt_checkmonitorpowerstate">D3DKMT_CHECKMONITORPOWERSTATE</a>

