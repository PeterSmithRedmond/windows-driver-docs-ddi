---
UID: NC:d3dkmthk.PDXGK_FSTATE_NOTIFICATION
title: PDXGK_FSTATE_NOTIFICATION (d3dkmthk.h)
description: Implemented by the client driver to issue a state notification.
ms.date: 10/07/2022
keywords: ["PDXGK_FSTATE_NOTIFICATION callback function"]
req.header: d3dkmthk.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: <= DISPATCH_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: display
ms.custom: engagement-fy23
f1_keywords:
 - PDXGK_FSTATE_NOTIFICATION
 - d3dkmthk/PDXGK_FSTATE_NOTIFICATION
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3dkmthk.h
api_name:
 - PDXGK_FSTATE_NOTIFICATION
product:
 - Windows
dev_langs:
 - c++
---

# PDXGK_FSTATE_NOTIFICATION callback function

## -description

Implemented by the client driver to issue a state notification.

## -parameters

### -param GraphicsDeviceHandle

An opaque handle which should be provided when making callbacks to the graphics device.

### -param ComponentIndex

The index of the component. Generally, this will be the index used by the graphics adapter. The exception is for LDA scenarios, where the HIWORD of the ComponentIndex indicates the adapter index, as is done when the graphics driver is called by graphics kernel for F-state changes in LDA scenarios.

### -param NewFState

The F-state to transition to.

### -param PreNotification

Indicates that a notification should be provided.

### -param PrivateHandle

An opaque handle which will be provided in any callbacks. This handle must be globally unique, therefore, a pointer to the calling driver's PDO or FDO should be used.

## -prototype

```cpp
//Declaration

PDXGK_FSTATE_NOTIFICATION PdxgkFstateNotification;

// Definition

VOID PdxgkFstateNotification
(
  PVOID GraphicsDeviceHandle
  ULONG ComponentIndex
  UINT NewFState
  BOOLEAN PreNotification
  PVOID PrivateHandle
)
{...}

```

## -remarks

All callbacks made from Dxgkrnl to this callback may be called at up to DISPATCH_LEVEL (e.g., the non-graphics driver should not block on any of these notifications). Callbacks will only be made for [DXGK_POWER_COMPONENT_SHARED](../d3dkmddi/ne-d3dkmddi-_dxgk_power_component_type.md) type power components.

Pre-notifications will be provided prior to transitioning F-states. Completion notification callbacks (PreNotification==FALSE) are issued as part of the graphics driver's [DxgkCbCompleteFStateTransition](../d3dkmddi/nc-d3dkmddi-dxgkcb_completefstatetransition.md) callback. That is, all shared power components will be notified of the F-state transition completion prior to DxgkCbCompleteFStateTransition returning.

## -see-also
