---
UID: NS:d3dkmthk._D3DKMDT_DISPLAYMODE_FLAGS
title: _D3DKMDT_DISPLAYMODE_FLAGS (d3dkmthk.h)
description: The D3DKMDT_DISPLAYMODE_FLAGS structure identifies attributes of a display mode.
old-location: display\d3dkmdt_displaymode_flags.htm
ms.date: 03/04/2022
keywords: ["D3DKMDT_DISPLAYMODE_FLAGS structure"]
ms.keywords: D3DKMDT_DISPLAYMODE_FLAGS, D3DKMDT_DISPLAYMODE_FLAGS structure [Display Devices], OpenGL_Structs_64aa66c8-8323-4cee-b437-16b8f3c361c8.xml, _D3DKMDT_DISPLAYMODE_FLAGS, d3dkmthk/D3DKMDT_DISPLAYMODE_FLAGS, display.d3dkmdt_displaymode_flags
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Windows
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
req.typenames: D3DKMDT_DISPLAYMODE_FLAGS
f1_keywords:
 - _D3DKMDT_DISPLAYMODE_FLAGS
 - d3dkmthk/_D3DKMDT_DISPLAYMODE_FLAGS
 - D3DKMDT_DISPLAYMODE_FLAGS
 - d3dkmthk/D3DKMDT_DISPLAYMODE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmthk.h
api_name:
 - _D3DKMDT_DISPLAYMODE_FLAGS
 - D3DKMDT_DISPLAYMODE_FLAGS
---

# _D3DKMDT_DISPLAYMODE_FLAGS structure

## -description

The D3DKMDT_DISPLAYMODE_FLAGS structure identifies attributes of a display mode.

## -struct-fields

### -field ValidatedAgainstMonitorCaps

A Boolean value that specifies whether the display mode is supported by the monitor that the display mode will be displayed on.

Setting this member is equivalent to setting the first bit of a 32-bit value (0x00000001).

A UINT value that specifies whether the display mode is supported by the monitor that the display mode will be displayed on.

Setting this member is equivalent to setting the first bit of a 32-bit value (0x00000001).

Supported starting with Windows 8.

### -field RoundedFakeMode

A Boolean value that specifies whether the display mode is rounded.

Setting this member is equivalent to setting the second bit of a 32-bit value (0x00000002).

A UINT value that specifies whether the display mode is rounded.

Setting this member is equivalent to setting the second bit of a 32-bit value (0x00000002).

Supported starting with Windows 8.

### -field ModePruningReason [in]

A value of type [D3DKMDT_MODE_PRUNING_REASON](ne-d3dkmthk-_d3dkmdt_mode_pruning_reason.md) that identifies the reason why the monitor either supports the display mode or does not support the display mode. The four bits are defined by one of the values in the **D3DKMDT_MODE_PRUNING_REASON** enumeration type and depend on the setting of the **ValidatedAgainstMonitorCaps** member. For more information about how the **ModePruningReason** value is set, see **D3DKMDT_MODE_PRUNING_REASON**.

Setting this member is equivalent to setting bits 4 through 7 of a 32-bit value (0x0000003C).

[in] A value of type [D3DKMDT_MODE_PRUNING_REASON](ne-d3dkmthk-_d3dkmdt_mode_pruning_reason.md) that identifies the reason why the monitor either supports the display mode or does not support the display mode. The four bits are defined by one of the values in the **D3DKMDT_MODE_PRUNING_REASON** enumeration type and depend on the setting of the **ValidatedAgainstMonitorCaps** member. For more information about how the **ModePruningReason** value is set, see **D3DKMDT_MODE_PRUNING_REASON**.
This member is equivalent to bits 4 through 7 of a 32-bit value (0x0000003C).

Supported starting with Windows 8.

### -field Stereo [in]

A UINT value that specifies whether stereo is supported by the monitor that the display mode will be displayed on.

Setting this member is equivalent to setting the eighth bit of a 32-bit value (0x00000080).

Supported starting with Windows 8.

### -field AdvancedScanCapable [in]

A UINT value that specifies whether the driver supports the advanced scan capability.

The driver reports support for this option in the current display mode by setting the **Type** member of the [D3DKMDT_VIDPN_SOURCE_MODE](../d3dkmdt/ns-d3dkmdt-_d3dkmdt_vidpn_source_mode.md) structure to **D3DKMDT_RMT_GRAPHICS_STEREO_ADVANCED_SCAN**.
Setting this member is equivalent to setting the ninth bit of a 32-bit value (0x00000100).

Supported starting with Windows 8.

### -field PreferredTiming

A UINT value that specifies whether the driver supports preferred timing.

### -field PhysicalModeSupported

A UINT value that specifies whether the driver supports physical mode.

### -field Reserved

This member is reserved and should be set to zero. Setting this member is equivalent to setting the remaining 28 bits (0xFFFFFFF0) of a 32-bit value to zeros.

This member is reserved and should be set to zero.

Setting this member is equivalent to setting the remaining 26 bits (0xFFFFFFC0) of a 32-bit value to zeros.

Supported starting with Windows 8.

### -field VirtualRefreshRate

A UINT value that specifies whether the driver supports virtual refresh rate.

## -see-also

[D3DKMDT_MODE_PRUNING_REASON](ne-d3dkmthk-_d3dkmdt_mode_pruning_reason.md)

[D3DKMT_DISPLAYMODE](ns-d3dkmthk-_d3dkmt_displaymode.md)
