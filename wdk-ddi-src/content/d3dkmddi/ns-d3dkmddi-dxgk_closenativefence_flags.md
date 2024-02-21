---
UID: NS:d3dkmddi._DXGK_CLOSENATIVEFENCE_FLAGS
tech.root: display
title: DXGK_CLOSENATIVEFENCE_FLAGS
ms.date: 03/21/2024
targetos: Windows
description: Learn more about DXGK_CLOSENATIVEFENCE_FLAGS.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3dkmddi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2
req.target-min-winversvr: 
req.target-type: 
req.typenames: DXGK_CLOSENATIVEFENCE_FLAGS
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3dkmddi.h
api_name:
 - _DXGK_CLOSENATIVEFENCE_FLAGS
 - DXGK_CLOSENATIVEFENCE_FLAGS
f1_keywords:
 - _DXGK_CLOSENATIVEFENCE_FLAGS
 - d3dkmddi/_DXGK_CLOSENATIVEFENCE_FLAGS
 - DXGK_CLOSENATIVEFENCE_FLAGS
 - d3dkmddi/DXGK_CLOSENATIVEFENCE_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - _DXGK_CLOSENATIVEFENCE_FLAGS
---

## -description

**DXGK_CLOSENATIVEFENCE_FLAGS** specifies flags to use when closing a native GPU fence.

## -struct-fields

### -field Reserved

Reserved for system use.

### -field Value

An alternative way to access the structure members.

## -remarks

For more information about native GPU fences, see [Native GPU fence objects](/windows-hardware/drivers/display/native-gpu-fence-objects).

## -see-also

[**DXGKARG_CLOSENATIVEFENCE**](ns-d3dkmddi-dxgkarg_closenativefence.md)

[**DxgkDdiCloseNativeFence**](nc-d3dkmddi-dxgkddi_closenativefence.md)
