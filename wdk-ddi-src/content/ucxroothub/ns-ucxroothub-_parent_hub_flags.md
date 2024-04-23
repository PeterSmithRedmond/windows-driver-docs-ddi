---
UID: NS:ucxroothub._PARENT_HUB_FLAGS
title: _PARENT_HUB_FLAGS (ucxroothub.h)
description: This structure is used by the HUB_INFO_FROM_PARENT structure to get hub information from the parent.
old-location: buses\_parent_hub_flags.htm
tech.root: usbref
ms.date: 02/08/2022
keywords: ["PARENT_HUB_FLAGS structure"]
ms.keywords: "*PPARENT_HUB_FLAGS, PARENT_HUB_FLAGS, PARENT_HUB_FLAGS union [Buses], _PARENT_HUB_FLAGS, buses._parent_hub_flags, ucxroothub/_PARENT_HUB_FLAGS"
req.header: ucxroothub.h
req.include-header: Ucxclass.h
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
req.typenames: PARENT_HUB_FLAGS, *PPARENT_HUB_FLAGS
f1_keywords:
 - _PARENT_HUB_FLAGS
 - ucxroothub/_PARENT_HUB_FLAGS
 - PPARENT_HUB_FLAGS
 - ucxroothub/PPARENT_HUB_FLAGS
 - PARENT_HUB_FLAGS
 - ucxroothub/PARENT_HUB_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ucxroothub.h
api_name:
 - _PARENT_HUB_FLAGS
 - PPARENT_HUB_FLAGS
 - PARENT_HUB_FLAGS
---

# _PARENT_HUB_FLAGS structure

## -description

This structure is used by the [HUB_INFO_FROM_PARENT](ns-ucxroothub-_hub_info_from_parent.md) structure to get hub information from the parent.

## -struct-fields

### -field AsUlong32

The size of structure represented as a LONG (32-bit) value.

### -field Flags

### -field Flags.DisableLpmForAllDownstreamDevices

Indicates that LPM should be disabled for all devices/hubs behind this hub.

### -field Flags.HubIsHighSpeedCapable

Indicates that the hub is high-speed capable.

### -field Flags.DisableUpdateMaxExitLatency

Indicates that UpdateMaxExitLatency should be disabled.

### -field Flags.DisableU1

Indicates that U1 transitions should be disabled.

### -field DisableLpmForAllDownstreamDevices

Indicates that LPM should be disabled for all devices/hubs behind this hub.

### -field HubIsHighSpeedCapable

Indicates that the hub is high-speed capable.

### -field DisableUpdateMaxExitLatency

Indicates that UpdateMaxExitLatency should be disabled.

### -field DisableU1

Indicates that U1 transitions should be disabled.

## -see-also

- [HUB_INFO_FROM_PARENT](ns-ucxroothub-_hub_info_from_parent.md)
