---
UID: NE:wditypes._WDI_POWER_MODE_REASON_CODE
title: _WDI_POWER_MODE_REASON_CODE (wditypes.h)
description: The WDI_POWER_MODE_REASON_CODE enumeration defines the reasons for entering the Power Save state.
old-location: netvista\wdi_power_mode_reason_code.htm
tech.root: netvista
ms.date: 05/02/2018
keywords: ["WDI_POWER_MODE_REASON_CODE enumeration"]
ms.keywords: WDI_POWER_MODE_REASON_CODE, WDI_POWER_MODE_REASON_CODE enumeration [Network Drivers Starting with Windows Vista], WDI_POWER_MODE_REASON_CODE_COMPLIANT_AP, WDI_POWER_MODE_REASON_CODE_COMPLIANT_P2P_DEVICE, WDI_POWER_MODE_REASON_CODE_LEGACY_P2P_DEVICE, WDI_POWER_MODE_REASON_CODE_NONCOMPLIANT_AP, WDI_POWER_MODE_REASON_CODE_NO_CHANGE, WDI_POWER_MODE_REASON_CODE_OTHERS, _WDI_POWER_MODE_REASON_CODE, netvista.wdi_power_mode_reason_code, netvista.wifi_power_mode_reason_code, wditypes/WDI_POWER_MODE_REASON_CODE, wditypes/WDI_POWER_MODE_REASON_CODE_COMPLIANT_AP, wditypes/WDI_POWER_MODE_REASON_CODE_COMPLIANT_P2P_DEVICE, wditypes/WDI_POWER_MODE_REASON_CODE_LEGACY_P2P_DEVICE, wditypes/WDI_POWER_MODE_REASON_CODE_NONCOMPLIANT_AP, wditypes/WDI_POWER_MODE_REASON_CODE_NO_CHANGE, wditypes/WDI_POWER_MODE_REASON_CODE_OTHERS
req.header: wditypes.hpp
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.typenames: WDI_POWER_MODE_REASON_CODE
f1_keywords:
 - _WDI_POWER_MODE_REASON_CODE
 - wditypes/_WDI_POWER_MODE_REASON_CODE
 - WDI_POWER_MODE_REASON_CODE
 - wditypes/WDI_POWER_MODE_REASON_CODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wditypes.hpp
api_name:
 - _WDI_POWER_MODE_REASON_CODE
 - WDI_POWER_MODE_REASON_CODE
---

# _WDI_POWER_MODE_REASON_CODE enumeration


## -description

> [!IMPORTANT]
> This topic is part of the [WDI driver model](/windows-hardware/drivers/network/wdi-miniport-driver-design-guide) released in Windows 10. The WDI driver model is in maintenance mode and will only receive high priority fixes. [WiFiCx](/windows-hardware/drivers/netcx/wifi-wdf-class-extension-wificx) is the Wi-Fi driver model released in Windows 11. We recommend that you use WiFiCx to take advantage of the latest  features.

The WDI_POWER_MODE_REASON_CODE enumeration defines the reasons for entering the Power Save state.

## -enum-fields

### -field WDI_POWER_MODE_REASON_CODE_NO_CHANGE

Device is initially in this state and has not changed since.

### -field WDI_POWER_MODE_REASON_CODE_LEGACY_P2P_DEVICE

WFD device is legacy.

### -field WDI_POWER_MODE_REASON_CODE_COMPLIANT_AP

AP is compliant.

### -field WDI_POWER_MODE_REASON_CODE_COMPLIANT_P2P_DEVICE

All connected WFD device can do PSM.

### -field WDI_POWER_MODE_REASON_CODE_OTHERS

Other reason.


### -field WDI_POWER_MODE_REASON_CODE_NONCOMPLIANT_AP

AP is not compliant. As to be in CAM.

