---
UID: NS:d3dkmthk._D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
title: _D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT (d3dkmthk.h)
description: The _D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT structure contains adapter, process, and support information for the D3DKMTGetProcessDeviceRemovalSupport function.
ms.date: 10/19/2018
keywords: ["D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT structure"]
ms.keywords: _D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT, D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT,
req.header: d3dkmthk.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
targetos: Windows
tech.root: display
f1_keywords:
 - _D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
 - d3dkmthk/_D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
 - D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
 - d3dkmthk/D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3dkmthk.h
api_name:
 - _D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
 - D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT
---

# _D3DKMT_GETPROCESSDEVICEREMOVALSUPPORT structure


## -description

Used to get process device removal support.

## -struct-fields

### -field hProcess

Handle to the process.

### -field AdapterLuid

Luid of Adapter that is potentially being detached.

### -field Support

Determines whether or not the process using the adapter can recover from graphics device removal.

