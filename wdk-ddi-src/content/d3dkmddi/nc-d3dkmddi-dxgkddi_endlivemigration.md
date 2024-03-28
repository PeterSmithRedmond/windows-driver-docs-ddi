---
UID: NC:d3dkmddi.DXGKDDI_ENDLIVEMIGRATION
tech.root: display
title: DXGKDDI_ENDLIVEMIGRATION
ms.date: 03/28/2024
targetos: Windows
description: Learn more about the DXGKDDI_ENDLIVEMIGRATION function.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3dkmddi.h
req.idl: 
req.include-header: 
req.irql: PASSIVE_LEVEL
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2 (WDDM 3.2)
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
 - d3dkmddi.h
api_name:
 - DXGKDDI_ENDLIVEMIGRATION
f1_keywords:
 - DXGKDDI_ENDLIVEMIGRATION
 - d3dkmddi/DXGKDDI_ENDLIVEMIGRATION
dev_langs:
 - c++
helpviewer_keywords:
 - DXGKDDI_ENDLIVEMIGRATION
---

## -description

*Dxgkrnl* calls KMD's **DxgkDdiEndLiveMigration** function to notify the driver that a live migration is ending.

## -parameters

### -param hAdapter

[in] A handle to a context block associated with a display adapter. The display miniport driver previously provided this handle to *Dxgkrnl* in the **MiniportDeviceContext** output parameter of the [**DXGKDDI_ADD_DEVICE**](../dispmprt/nc-dispmprt-dxgkddi_add_device.md) function.

### -param vfIndex

[in] Identifies the virtual function / vDEV being referenced. This index value localizes to the specific virtual device.

## -returns

**DxgkDdiEndLiveMigration** returns STATUS_SUCCESS if it succeeds; otherwise, it returns an appropriate NTSTATUS code.

## -remarks

**DxgkDdiEndLiveMigration** is called when there is no more need for migration configuration on the specified VF. All scheduling and state should return to a non-migrating configuration.

For more information, see [Live migration on GPU-P devices](/windows-hardware/drivers/display/live-migration-on-gpup-devices).

## -see-also

[**DxgkDdiPrepareLiveMigration**](nc-d3dkmddi-dxgkddi_preparelivemigration.md)
