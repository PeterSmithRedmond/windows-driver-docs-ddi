---
UID: NC:d3dkmddi.DXGKDDI_CREATEPROTECTEDSESSION
title: DXGKDDI_CREATEPROTECTEDSESSION (d3dkmddi.h)
description: The DXGKDDI_CREATEPROTECTEDSESSION callback function creates a protected session and returns STATUS_SUCCESS on successful completion.
old-location: display\dxgkddi_createprotectedsession.htm
ms.date: 05/10/2018
keywords: ["DXGKDDI_CREATEPROTECTEDSESSION callback function"]
ms.keywords: DXGKDDI_CREATEPROTECTEDSESSION, DXGKDDI_CREATEPROTECTEDSESSION callback, DXGKDDI_CREATEPROTECTEDSESSION callback function [Display Devices], d3dkmddi/DXGKDDI_CREATEPROTECTEDSESSION, display.dxgkddi_createprotectedsession
req.header: d3dkmddi.h
req.include-header: 
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
req.irql: requires_(PASSIVE_LEVEL)
targetos: Windows
tech.root: display
req.typenames: 
f1_keywords:
 - DXGKDDI_CREATEPROTECTEDSESSION
 - d3dkmddi/DXGKDDI_CREATEPROTECTEDSESSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - d3dkmddi.h
api_name:
 - DXGKDDI_CREATEPROTECTEDSESSION
---

# DXGKDDI_CREATEPROTECTEDSESSION callback function


## -description

Used to create a protected session.

## -parameters

### -param hAdapter

A handle to the adapter.

### -param pCreateProtectedSession

A pointer to the arguments used to create a protected session.

## -returns

Returns STATUS_SUCCESS if completed successfully.

