---
UID: NE:dot11wificxtypes._WDI_SAE_REQUEST_TYPE
tech.root: netvista
title: WDI_SAE_REQUEST_TYPE (dot11wificxtypes.h)
ms.date: 07/10/2023
targetos: Windows
description: The WDI_SAE_REQUEST_TYPE enum defines the type of SAE request frame to send to the BSSID.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: dot11wificxtypes.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dot11wificxtypes.h
api_name:
 - _WDI_SAE_REQUEST_TYPE
 - WDI_SAE_REQUEST_TYPE
f1_keywords:
 - _WDI_SAE_REQUEST_TYPE
 - dot11wificxtypes/_WDI_SAE_REQUEST_TYPE
 - WDI_SAE_REQUEST_TYPE
 - dot11wificxtypes/WDI_SAE_REQUEST_TYPE
dev_langs:
 - c++
---

## -description

> [!IMPORTANT]
> This topic is part of the [WiFiCx driver model](/windows-hardware/drivers/netcx/wifi-wdf-class-extension-wificx). WiFiCx is the Wi-Fi driver model released in Windows 11. We recommend that you use WiFiCx to take advantage of the latest  features. The previous Wi-Fi driver model [WDI](/windows-hardware/drivers/network/wdi-miniport-driver-design-guide) is in maintenance mode and will only receive high priority fixes.

The **WDI_SAE_REQUEST_TYPE** enumeration defines the type of Simultaneous Authentication of Equals (SAE) request frame to send to the BSSID.

## -enum-fields

### -field WDI_SAE_REQUEST_TYPE_COMMIT_PARAMS:0

Send a Commit request. SAECommitRequest will be included.

### -field WDI_SAE_REQUEST_TYPE_CONFIRM_PARAMS:1

Send a Confirm request. SAEConfirmRequest will be included.

### -field WDI_SAE_REQUEST_TYPE_FAILURE:2

Request SAE authentication parameters failed. SAEStatus will be included.

### -field WDI_SAE_REQUEST_TYPE_SUCCESS:3

Request SAE authentication parameters succeeded.

### -field WDI_SAE_REQUEST_TYPE_COMMIT_H2E_PARAMS:4

Send a Commit Request using H2E. When Anti-Clogging token is specified, it will be encoded as Anti-Clogging Element instead of a field.

## -remarks

This enumeration is a value in the [OID_WDI_SET_SAE_AUTH_PARAMS](/windows-hardware/drivers/netcx/oid-wdi-set-sae-auth-params) command.

## -see-also

[WPA3-SAE Authentication](/windows-hardware/drivers/netcx/wificx-wpa3-sae-authentication)

[OID_WDI_SET_SAE_AUTH_PARAMS](/windows-hardware/drivers/network/oid-wdi-set-sae-auth-params)


