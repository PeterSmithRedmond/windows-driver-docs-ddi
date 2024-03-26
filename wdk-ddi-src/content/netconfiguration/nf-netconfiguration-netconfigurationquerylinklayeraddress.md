---
UID: NF:netconfiguration.NetConfigurationQueryLinkLayerAddress
title: NetConfigurationQueryLinkLayerAddress function (netconfiguration.h)
description: The NetConfigurationQueryLinkLayerAddress function retrieves the software-configurable link layer address that was stored in the registry for a NIC.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetConfigurationQueryLinkLayerAddress function"]
ms.keywords: NetConfigurationQueryLinkLayerAddress
req.header: netconfiguration.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.23
req.umdf-ver: 2.33 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.alt-api: 
req.alt-loc: 
targetos: Windows
f1_keywords:
 - NetConfigurationQueryLinkLayerAddress
 - netconfiguration/NetConfigurationQueryLinkLayerAddress
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netconfiguration.h
api_name:
 - NetConfigurationQueryLinkLayerAddress
---

# NetConfigurationQueryLinkLayerAddress function


## -description

The **NetConfigurationQueryLinkLayerAddress** function retrieves the software-configurable link layer address that was stored in the registry for a NIC.

## -parameters

### -param Configuration [_In_]

Handle to a NETCONFIGURATION object that represents an opened registry key.

### -param LinkLayerAddress [_Out_]

A pointer to a NET_ADAPTER_LINK_LAYER_ADDRESS object that represents the link layer address stored in the registry key.

## -returns

The function returns STATUS_SUCCESS if the operation succeeds. Otherwise, this function may return an appropriate NTSTATUS error code.

## -remarks

The client driver obtains a handle to a NETCONFIGURATION object by calling [NetAdapterOpenConfiguration](../netadapter/nf-netadapter-netadapteropenconfiguration.md) or [NetConfigurationOpenSubConfiguration](nf-netconfiguration-netconfigurationopensubconfiguration.md).

## -see-also

