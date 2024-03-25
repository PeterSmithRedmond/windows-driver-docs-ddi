---
UID: NF:d3dkmthk.D3DKMTGetProcessDeviceRemovalSupport
title: D3DKMTGetProcessDeviceRemovalSupport function (d3dkmthk.h)
description: The D3DKMTGetProcessDeviceRemovalSupport function determines whether a process using the specified adapter can recover from graphics device removal.
ms.date: 02/25/2022
keywords: ["D3DKMTGetProcessDeviceRemovalSupport function"]
ms.keywords: D3DKMTGetProcessDeviceRemovalSupport
req.header: d3dkmthk.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: display
f1_keywords:
 - D3DKMTGetProcessDeviceRemovalSupport
 - d3dkmthk/D3DKMTGetProcessDeviceRemovalSupport
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Gdi32.dll
api_name:
 - D3DKMTGetProcessDeviceRemovalSupport
---

# D3DKMTGetProcessDeviceRemovalSupport function

## -description

Used to get process device removal support.

## -parameters

### -param unnamedParam1

Pointer to a [D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT](ns-d3dkmthk-_d3dkmt_getprocessdeviceremovalsupport.md) structure.

## -returns

This function returns **NTSTATUS**.
