---
UID: NF:wificx.WIFI_DEVICE_CAPABILITIES_INIT
tech.root: netvista
title: WIFI_DEVICE_CAPABILITIES_INIT
ms.date: 03/06/2024
targetos: Windows
description: The WIFI_DEVICE_CAPABILITIES_INIT function initializes a WIFI_DEVICE_CAPABILITIES structure.
prerelease: 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wificx.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wificx.h
api_name:
 - WIFI_DEVICE_CAPABILITIES_INIT
f1_keywords:
 - WIFI_DEVICE_CAPABILITIES_INIT
 - wificx/WIFI_DEVICE_CAPABILITIES_INIT
dev_langs:
 - c++
helpviewer_keywords:
 - WIFI_DEVICE_CAPABILITIES_INIT
---

## -description

The **WIFI_DEVICE_CAPABILITIES_INIT** function initializes a [**WIFI_DEVICE_CAPABILITIES**](ns-wificx-wifi_device_capabilities.md) structure.

## -parameters

### -param Capabilities

[_Out_] A pointer to a client driver-allocated **WIFI_DEVICE_CAPABILITIES** structure.

## -remarks

This function zeroes out the memory of the **WIFI_DEVICE_CAPABILITIES** structure, then fills in the **Size** member. Client drivers must then call [**WifiDeviceSetDeviceCapabilities**](nf-wificx-wifidevicesetdevicecapabilities.md) to report device capabilities to WiFiCx.

## -see-also

[**WIFI_DEVICE_CAPABILITIES**](ns-wificx-wifi_device_capabilities.md)

[**WifiDeviceSetDeviceCapabilities**](nf-wificx-wifidevicesetdevicecapabilities.md) 