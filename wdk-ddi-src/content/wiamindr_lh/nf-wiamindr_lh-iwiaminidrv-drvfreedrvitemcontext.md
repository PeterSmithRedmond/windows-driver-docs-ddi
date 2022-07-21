---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvFreeDrvItemContext
title: IWiaMiniDrv::drvFreeDrvItemContext (wiamindr_lh.h)
description: The IWiaMiniDrv::drvFreeDrvItemContext method frees a device-specific context.
tech.root: image
ms.date: 07/21/2022
keywords: ["IWiaMiniDrv::drvFreeDrvItemContext"]
ms.keywords: IWiaMiniDrv interface [Imaging Devices],drvFreeDrvItemContext method, IWiaMiniDrv.drvFreeDrvItemContext, IWiaMiniDrv::drvFreeDrvItemContext, MiniDrv_59a7d220-cd1d-4cc2-870a-3260feaba7e9.xml, drvFreeDrvItemContext, drvFreeDrvItemContext method [Imaging Devices], drvFreeDrvItemContext method [Imaging Devices],IWiaMiniDrv interface, image.iwiaminidrv_drvfreedrvitemcontext, wiamindr_lh/IWiaMiniDrv::drvFreeDrvItemContext
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
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
req.typenames: 
f1_keywords:
 - IWiaMiniDrv::drvFreeDrvItemContext
 - wiamindr_lh/IWiaMiniDrv::drvFreeDrvItemContext
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wiamindr_lh.h
api_name:
 - IWiaMiniDrv::drvFreeDrvItemContext
---

## -description

The **IWiaMiniDrv::drvFreeDrvItemContext** method frees a device-specific context.

## -parameters

### -param __MIDL__IWiaMiniDrv0056

*lFlags* [in]

Reserved.

### -param __MIDL__IWiaMiniDrv0057

*pSpecContext* [in]

Points to a device-specific context.

### -param __MIDL__IWiaMiniDrv0058

*plDevErrVal* [out]

Points to a memory location that will receive a status code for this method. If this method returns **S_OK**, the value stored will be zero. Otherwise, a minidriver-specific error code will be stored at the location pointed to by this parameter.

## -returns

On success, the method should return **S_OK** and clear the device error value pointed to by *plDevErrVal*. If the method fails, it should return a standard COM error code and place a minidriver-specific error code in the memory pointed to by *plDevErrVal*.

The value pointed to by *plDevErrVal* can be converted to a string by calling  [IWiaMiniDrv::drvGetDeviceErrorStr](./nf-wiamindr_lh-iwiaminidrv-drvgetdeviceerrorstr.md).

## -remarks

When a driver item is deleted, the WIA service frees the driver item context. This method informs the minidriver that the context is ready to be freed. The minidriver should free any memory that it allocated for the context. For example, in  [IWiaMiniDrv::drvReadItemProperties](./nf-wiamindr_lh-iwiaminidrv-drvreaditemproperties.md), a camera minidriver might allocate a cache to store the thumbnail for an item, and store a pointer to this cache in the driver item context. The minidriver would then free the cache in this method.

## -see-also

 [IWiaMiniDrv](./nn-wiamindr_lh-iwiaminidrv.md)

 [IWiaMiniDrv::drvGetDeviceErrorStr](./nf-wiamindr_lh-iwiaminidrv-drvgetdeviceerrorstr.md)

 [IWiaMiniDrv::drvReadItemProperties](./nf-wiamindr_lh-iwiaminidrv-drvreaditemproperties.md)
