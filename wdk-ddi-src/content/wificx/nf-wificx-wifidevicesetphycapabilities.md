---
UID: NF:wificx.WifiDeviceSetPhyCapabilities
tech.root: netvista
title: WifiDeviceSetPhyCapabilities (wificx.h)
ms.date: 03/06/2024
ms.topic: language-reference
targetos: Windows
description: The WifiDeviceSetPhyCapabilities function sets the PHY capabilities for a WiFiCx device.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wificx.h
req.idl: 
req.include-header: 
req.irql: PASSIVE_LEVEL
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 
req.target-min-winversvr: Windows Server 2022
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
 - WifiDeviceSetPhyCapabilities
f1_keywords:
 - WifiDeviceSetPhyCapabilities
 - wificx/WifiDeviceSetPhyCapabilities
dev_langs:
 - c++
---

## -description

The **WifiDeviceSetPhyCapabilities** function sets the PHY capabilities for a WiFiCx device.

## -parameters

### -param Device

A handle to a framework device object the client driver obtained from a previous call to [**WdfDeviceCreate**](../wdfdevice/nf-wdfdevice-wdfdevicecreate.md).

### -param PhyCapabilities

A pointer to a client driver-allocated and initialized [**WIFI_PHY_CAPABILITIES**](ns-wificx-wifi_wifidirect_capabilities.md) structure.

## -returns

Returns STATUS_SUCCESS if the operation succeeds. Otherwise, this function may return an appropriate NTSTATUS error code.

## -remarks

Client drivers typically call **WifiDeviceSetPhyCapabilities** within [*EvtDevicePrepareHardware*](../wdfdevice/nc-wdfdevice-evt_wdf_device_prepare_hardware.md).

Call [**WIFI_PHY_CAPABILITIES_INIT**](nf-wificx-wifi_phy_capabilities_init.md) to initialize the **WIFI_PHY_CAPABILITIES** structure and fill in its **Size** field. Then call **WifiDeviceSetPhyCapabilities** to report PHY capabilities to WiFiCx.

For more information see [Default (station) adapter creation flow](/windows-hardware/drivers/netcx/writing-a-wificx-client-driver#default-(station)-adapter-creation-flow).

## -see-also

[**WIFI_PHY_CAPABILITIES_INIT**](nf-wificx-wifi_phy_capabilities_init.md)

[**WIFI_PHY_CAPABILITIES**](ns-wificx-wifi_wifidirect_capabilities.md)

[Default (station) adapter creation flow](/windows-hardware/drivers/netcx/writing-a-wificx-client-driver#default-(station)-adapter-creation-flow)