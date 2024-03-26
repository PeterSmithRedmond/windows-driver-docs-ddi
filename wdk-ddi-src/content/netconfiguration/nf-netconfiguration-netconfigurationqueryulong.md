---
UID: NF:netconfiguration.NetConfigurationQueryUlong
title: NetConfigurationQueryUlong function (netconfiguration.h)
description: Retrieves the specified unsigned long word (REG_DWORD) data from the adapter configuration object and copies the data to a specified location.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetConfigurationQueryUlong function"]
ms.keywords: NetConfigurationQueryUlong
req.header: netconfiguration.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.21
req.umdf-ver: 2.33 
req.lib: NetAdapterCxStub.lib
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
 - NetConfigurationQueryUlong
 - netconfiguration/NetConfigurationQueryUlong
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netconfiguration.h
api_name:
 - NetConfigurationQueryUlong
---

# NetConfigurationQueryUlong function


## -description

Retrieves the specified unsigned long word (REG_DWORD) data from the adapter configuration object and copies the data to a specified location.

## -parameters

### -param Configuration [_In_]

Handle to a NETCONFIGURATION object that represents an opened registry key.

### -param Flags [_In_]

A valid bitwise OR of [NET_CONFIGURATION_QUERY_ULONG_FLAGS](ne-netconfiguration-_net_configuration_query_ulong_flags.md)-typed flags.

### -param ValueName [_In_]

A pointer to a [**UNICODE_STRING**](/windows/win32/api/ntdef/ns-ntdef-_unicode_string) structure that contains a name for the ULONG value.

### -param Value [_Out_]

A pointer to a location that receives the data that is assigned to the value that *ValueName* specifies.

## -returns

The function returns STATUS_SUCCESS if the operation succeeds. Otherwise, this function may return an appropriate NTSTATUS error code.

## -remarks

The client driver obtains a handle to a NETCONFIGURATION object by calling [NetAdapterOpenConfiguration](../netadapter/nf-netadapter-netadapteropenconfiguration.md) or [NetConfigurationOpenSubConfiguration](nf-netconfiguration-netconfigurationopensubconfiguration.md).

## -see-also
