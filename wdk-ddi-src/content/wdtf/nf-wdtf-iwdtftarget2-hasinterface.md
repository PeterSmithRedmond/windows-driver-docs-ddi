---
UID: NF:wdtf.IWDTFTarget2.HasInterface
title: IWDTFTarget2::HasInterface (wdtf.h)
description: Determines whether the target supports a given interface.
old-location: dtf\iwdtftarget2_hasinterface.htm
tech.root: dtf
ms.date: 08/14/2023
keywords: ["IWDTFTarget2::HasInterface"]
ms.keywords: HasInterface, HasInterface method [Windows Device Testing Framework], HasInterface method [Windows Device Testing Framework],IWDTFTarget2 interface, IWDTFTarget2 interface [Windows Device Testing Framework],HasInterface method, IWDTFTarget2.HasInterface, IWDTFTarget2::HasInterface, Microsoft.WDTF.IWDTFTarget2.HasInterface, Microsoft::WDTF::IWDTFTarget2::HasInterface, dtf.iwdtftarget2_hasinterface, wdtf/IWDTFTarget2::HasInterface
req.header: wdtf.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTF.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTF.Interop.metadata_dll
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IWDTFTarget2::HasInterface
 - wdtf/IWDTFTarget2::HasInterface
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WDTF.Interop.metadata_dll.dll
api_name:
 - IWDTFTarget2::HasInterface
---

# IWDTFTarget2::HasInterface

## -description

Determines whether the target supports a given interface.

## -parameters

### -param WDTFInterfaceName

### -param Args

### -param MonikerSuffix [in, optional]

An optional moniker that defines more options about how the interface should be instantiated. 

This parameter is not yet implemented. Set <i>MonikerSuffix </i>to a <b>VARIANT</b> that 
contains <b>VT_EMPTY</b>.

### -param pResult [out, retval]

True if the target supports the interface; otherwise false.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdtf/nn-wdtf-iwdtftarget2">IWDTFTarget2</a>
