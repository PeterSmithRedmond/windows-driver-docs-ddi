---
UID: NE:pointofservicedriverinterface._MsrAuthenticationProtocol
title: MsrAuthenticationProtocol (pointofservicedriverinterface.h)
description: This enumeration defines magnetic stripe reader (MSR) authentication protocols.
tech.root: pos
ms.date: 01/03/2023
keywords: ["MsrAuthenticationProtocol enumeration"]
ms.keywords: MsrAuthenticationProtocol, MsrAuthenticationProtocol enumeration, MsrAuthenticationProtocolType, MsrAuthenticationProtocolType enumeration, MsrAuthenticationProtocolType_ChallengeResponse, MsrAuthenticationProtocolType_None, _MsrAuthenticationProtocol, pointofservicedriverinterface/MsrAuthenticationProtocolType, pointofservicedriverinterface/MsrAuthenticationProtocolType_ChallengeResponse, pointofservicedriverinterface/MsrAuthenticationProtocolType_None, pos.msrauthenticationprotocoltype
req.header: pointofservicedriverinterface.h
req.include-header: Pointofservicedriverinterface.h
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
req.typenames: MsrAuthenticationProtocolType
f1_keywords:
 - _MsrAuthenticationProtocol
 - pointofservicedriverinterface/_MsrAuthenticationProtocol
 - MsrAuthenticationProtocolType
 - pointofservicedriverinterface/MsrAuthenticationProtocolType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - pointofservicedriverinterface.h
api_name:
 - _MsrAuthenticationProtocol
 - MsrAuthenticationProtocolType
---

## -description

This enumeration defines magnetic stripe reader (MSR) authentication protocols.

## -enum-fields

### -field MsrAuthenticationProtocolType_None

Authentication is not supported.

### -field MsrAuthenticationProtocolType_ChallengeResponse

Challenge-response authentication is supported.

## -remarks

Password authentication is an example of challenge-response authentication.
