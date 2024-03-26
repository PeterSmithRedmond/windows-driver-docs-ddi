---
UID: NF:netconfiguration.NetConfigurationClose
title: NetConfigurationClose function (netconfiguration.h)
description: Releases the handle to the registry key that is associated with an adapter configuration object and then deletes the adapter configuration object.
tech.root: netvista
ms.date: 02/07/2018
keywords: ["NetConfigurationClose function"]
ms.keywords: NetConfigurationClose
req.header: netconfiguration.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.21
req.umdf-ver: 2.33 
req.lib: netadaptercxstub.lib
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
 - NetConfigurationClose
 - netconfiguration/NetConfigurationClose
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netconfiguration.h
api_name:
 - NetConfigurationClose
---

# NetConfigurationClose function


## -description

Releases the handle to the registry key that is associated with an adapter configuration object and then deletes the adapter configuration object.

## -parameters

### -param Configuration [_In_]

A handle to an adapter configuration object opened in a prior call to [NetAdapterOpenConfiguration](../netadapter/nf-netadapter-netadapteropenconfiguration.md) or [NetConfigurationOpenSubConfiguration](nf-netconfiguration-netconfigurationopensubconfiguration.md).

## -remarks

**NetConfigurationClose** is an alias of [WdfObjectDelete](../wdfobject/nf-wdfobject-wdfobjectdelete.md). Because the configuration object, like all NetAdapterCx objects, is a WDF object, you can use [WdfObjectDelete](../wdfobject/nf-wdfobject-wdfobjectdelete.md) interchangeably.

## -see-also

[NetAdapterOpenConfiguration](../netadapter/nf-netadapter-netadapteropenconfiguration.md)

[NetConfigurationOpenSubConfiguration](nf-netconfiguration-netconfigurationopensubconfiguration.md)

