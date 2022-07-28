---
UID: NS:ntifs._TOKEN_PRIMARY_GROUP
title: TOKEN_PRIMARY_GROUP (ntifs.h)
description: TOKEN_PRIMARY_GROUP specifies a group security identifier (SID) for an access token.
old-location: ifsk\token_primary_group.htm
tech.root: ifsk
ms.date: 07/26/2022
keywords: ["TOKEN_PRIMARY_GROUP structure"]
ms.keywords: "*PTOKEN_PRIMARY_GROUP, PTOKEN_PRIMARY_GROUP, PTOKEN_PRIMARY_GROUP structure pointer [Installable File System Drivers], TOKEN_PRIMARY_GROUP, TOKEN_PRIMARY_GROUP structure [Installable File System Drivers], _TOKEN_PRIMARY_GROUP, ifsk.token_primary_group, ntifs/PTOKEN_PRIMARY_GROUP, ntifs/TOKEN_PRIMARY_GROUP, securitystructures_8d3bc1f9-abc5-4ac3-8351-cf2c56db6a20.xml"
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: TOKEN_PRIMARY_GROUP, *PTOKEN_PRIMARY_GROUP
f1_keywords:
 - _TOKEN_PRIMARY_GROUP
 - ntifs/_TOKEN_PRIMARY_GROUP
 - PTOKEN_PRIMARY_GROUP
 - ntifs/PTOKEN_PRIMARY_GROUP
 - TOKEN_PRIMARY_GROUP
 - ntifs/TOKEN_PRIMARY_GROUP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - _TOKEN_PRIMARY_GROUP
 - PTOKEN_PRIMARY_GROUP
 - TOKEN_PRIMARY_GROUP
---

# TOKEN_PRIMARY_GROUP structure

## -description

The **TOKEN_PRIMARY_GROUP** structure specifies a group security identifier (SID) for an access token.

## -struct-fields

### -field PrimaryGroup

Pointer to a SID structure representing a group that will become the primary group of any objects created by a process using this access token. The SID must be one of the group SIDs already in the token.

## -see-also

[**SID**](ns-ntifs-_sid.md)

[**SeQueryInformationToken**](nf-ntifs-sequeryinformationtoken.md)

[**TOKEN_INFORMATION_CLASS**](ne-ntifs-_token_information_class.md)

[**ZwQueryInformationToken**](nf-ntifs-zwqueryinformationtoken.md)

[**ZwSetInformationToken**](nf-ntifs-zwsetinformationtoken.md)
