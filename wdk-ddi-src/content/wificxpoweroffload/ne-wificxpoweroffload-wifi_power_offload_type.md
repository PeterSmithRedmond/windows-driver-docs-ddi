---
UID: NE:wificxpoweroffload._WIFI_POWER_OFFLOAD_TYPE
tech.root: netvista
title: WIFI_POWER_OFFLOAD_TYPE (wificxpoweroffload.h)
ms.date: 03/04/2024
targetos: Windows
description: The WIFI_POWER_OFFLOAD_TYPE enumeration specifies the type for a low power offload protocol offload to a WiFiCx network adapter.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wificxpoweroffload.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 
req.target-min-winversvr: Windows Server 2022
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wificxpoweroffload.h
api_name:
 - _WIFI_POWER_OFFLOAD_TYPE
 - WIFI_POWER_OFFLOAD_TYPE
f1_keywords:
 - _WIFI_POWER_OFFLOAD_TYPE
 - wificxpoweroffload/_WIFI_POWER_OFFLOAD_TYPE
 - WIFI_POWER_OFFLOAD_TYPE
 - wificxpoweroffload/WIFI_POWER_OFFLOAD_TYPE
dev_langs:
 - c++
---

## -description

The **WIFI_POWER_OFFLOAD_TYPE** enumeration specifies the type for a low power offload protocol offload to a WiFiCx network adapter.

## -enum-fields

### -field WifiPowerOffloadType80211RsnRekey:1

The power offload is the 802.11 RSN rekey protocol.

### -field WifiPowerOffloadTypeWakeOnIncomingActionFrame:2

The power offload is for waking on incoming action frame reception.

## -remarks

Call [**WifiPowerOffloadGetType**](nf-wificxpoweroffload-wifipoweroffloadgettype.md) to get the type for a low power protocol offload to a WiFiCx network adapter.

## -see-also

[**WifiPowerOffloadGetType**](nf-wificxpoweroffload-wifipoweroffloadgettype.md)