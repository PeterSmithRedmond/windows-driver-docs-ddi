---
UID: NE:netconfiguration._NET_CONFIGURATION_QUERY_ULONG_FLAGS
title: _NET_CONFIGURATION_QUERY_ULONG_FLAGS (netconfiguration.h)
description: The NET_CONFIGURATION_QUERY_ULONG_FLAGS enumeration is used as an input parameter to the NetConfigurationQueryUlong function.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_CONFIGURATION_QUERY_ULONG_FLAGS enumeration"]
ms.keywords: _NET_CONFIGURATION_QUERY_ULONG_FLAGS, NET_CONFIGURATION_QUERY_ULONG_FLAGS,
req.header: netconfiguration.h
req.include-header: netadaptercx.h
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.21
req.umdf-ver: 2.33 
req.ddi-compliance: 
req.max-support: 
req.alt-api: 
req.alt-loc: 
req.typenames: NET_CONFIGURATION_QUERY_ULONG_FLAGS
targetos: Windows
f1_keywords:
 - _NET_CONFIGURATION_QUERY_ULONG_FLAGS
 - netconfiguration/_NET_CONFIGURATION_QUERY_ULONG_FLAGS
 - NET_CONFIGURATION_QUERY_ULONG_FLAGS
 - netconfiguration/NET_CONFIGURATION_QUERY_ULONG_FLAGS
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netconfiguration.h
api_name:
 - _NET_CONFIGURATION_QUERY_ULONG_FLAGS
 - NET_CONFIGURATION_QUERY_ULONG_FLAGS
---

# _NET_CONFIGURATION_QUERY_ULONG_FLAGS enumeration


## -description

The **NET_CONFIGURATION_QUERY_ULONG_FLAGS** enumeration is used as an input parameter to the [NetConfigurationQueryUlong](nf-netconfiguration-netconfigurationqueryulong.md) function.

## -enum-fields

### -field NET_CONFIGURATION_QUERY_ULONG_NO_FLAGS:0x00000000 

No flags are set.

### -field NET_CONFIGURATION_QUERY_ULONG_MAY_BE_STORED_AS_HEX_STRING:0x00000001 

Specifies that the ULONG may be stored in the configuration database as a string in hex format.

## -remarks

## -see-also

[NetConfigurationQueryUlong](nf-netconfiguration-netconfigurationqueryulong.md)

