---
UID: NS:d3dkmddi._DXGKARG_CONTROLINTERRUPT2
title: DXGKARG_CONTROLINTERRUPT2 (d3dkmddi.h)
description: Learn more about the DXGKARG_CONTROLINTERRUPT2 structure.
ms.date: 03/24/2020
ms.keywords: DXGKARG_CONTROLINTERRUPT2, DXGKARG_CONTROLINTERRUPT2 structure [Display Devices], DXGKARG_CONTROLINTTERUPT2, DXGKARG_CONTROLINTTERUPT2 structure [Display Devices], _DXGKARG_CONTROLINTERRUPT2, d3dkmddi/DXGKARG_CONTROLINTERRUPT2, display.dxgkarg_controlinterrupt2
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
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
req.typenames: DXGKARG_CONTROLINTERRUPT2
f1_keywords:
 - _DXGKARG_CONTROLINTERRUPT2
 - d3dkmddi/_DXGKARG_CONTROLINTERRUPT2
 - DXGKARG_CONTROLINTERRUPT2
 - d3dkmddi/DXGKARG_CONTROLINTERRUPT2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmddi.h
api_name:
 - _DXGKARG_CONTROLINTERRUPT2
 - DXGKARG_CONTROLINTERRUPT2
---

# DXGKARG_CONTROLINTERRUPT2 structure

## -description

The **DXGKARG_CONTROLINTERRUPT2** structure is used in [**DxgkDdi_ControlInterrupt2**](./nc-d3dkmddi-dxgkddi_controlinterrupt2.md) calls to describe the state of interrupts.

## -struct-fields

### -field InterruptType

A [**DXGK_INTERRUPT_TYPE**](./ne-d3dkmddi-_dxgk_interrupt_type.md) enumeration that indicates the type of interrupt.

### -field InterruptState

A [**DXGK_INTERRUPT_STATE**](./ne-d3dkmddi-_dxgk_interrupt_state.md) enumeration that indicates whether interrupts are enabled for the driver.

### -field CrtcVsyncState

A [**DXGK_CRTC_VSYNC_STATE**](./ne-d3dkmddi-_dxgk_crtc_vsync_state.md) enumeration that indicates whether VSYNCs are enabled if interrupts are also enabled for the driver.

## -remarks

**InterruptState** and **CrtcVsyncState** are members of a union.

## -see-also

[**DXGK_INTERRUPT_STATE**](./ne-d3dkmddi-_dxgk_interrupt_state.md)

[**DXGK_INTERRUPT_TYPE**](./ne-d3dkmddi-_dxgk_interrupt_type.md)

[**DXGKARG_CONTROLINTERRUPT3**](ns-d3dkmddi-dxgkarg_controlinterrupt3.md)

[**DxgkDdi_ControlInterrupt2**](./nc-d3dkmddi-dxgkddi_controlinterrupt2.md)

[**DxgkDdi_ControlInterrupt3**](./nc-d3dkmddi-dxgkddi_controlinterrupt3.md)
