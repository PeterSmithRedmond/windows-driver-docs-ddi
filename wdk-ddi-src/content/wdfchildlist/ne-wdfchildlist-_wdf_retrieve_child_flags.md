---
UID: NE:wdfchildlist._WDF_RETRIEVE_CHILD_FLAGS
title: _WDF_RETRIEVE_CHILD_FLAGS (wdfchildlist.h)
description: The WDF_RETRIEVE_CHILD_FLAGS enumeration defines flags that a driver can set before calling WdfChildListBeginIteration.
old-location: wdf\wdf_retrieve_child_flags.htm
tech.root: wdf
ms.date: 02/26/2018
keywords: ["WDF_RETRIEVE_CHILD_FLAGS enumeration"]
ms.keywords: DFDeviceObjectChildListRef_f82096f7-f6f9-4e49-a3e3-2641f60f98d9.xml, WDF_RETRIEVE_CHILD_FLAGS, WDF_RETRIEVE_CHILD_FLAGS enumeration, WdfRetrieveAddedChildren, WdfRetrieveAllChildren, WdfRetrieveMissingChildren, WdfRetrievePendingChildren, WdfRetrievePresentChildren, WdfRetrieveUnspecified, _WDF_RETRIEVE_CHILD_FLAGS, kmdf.wdf_retrieve_child_flags, wdf.wdf_retrieve_child_flags, wdfchildlist/WDF_RETRIEVE_CHILD_FLAGS, wdfchildlist/WdfRetrieveAddedChildren, wdfchildlist/WdfRetrieveAllChildren, wdfchildlist/WdfRetrieveMissingChildren, wdfchildlist/WdfRetrievePendingChildren, wdfchildlist/WdfRetrievePresentChildren, wdfchildlist/WdfRetrieveUnspecified
req.header: wdfchildlist.h
req.include-header: Wdf.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
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
req.typenames: WDF_RETRIEVE_CHILD_FLAGS
f1_keywords:
 - _WDF_RETRIEVE_CHILD_FLAGS
 - wdfchildlist/_WDF_RETRIEVE_CHILD_FLAGS
 - WDF_RETRIEVE_CHILD_FLAGS
 - wdfchildlist/WDF_RETRIEVE_CHILD_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdfchildlist.h
api_name:
 - _WDF_RETRIEVE_CHILD_FLAGS
 - WDF_RETRIEVE_CHILD_FLAGS
---

# _WDF_RETRIEVE_CHILD_FLAGS enumeration


## -description

<p class="CCE_Message">[Applies to KMDF only]</p>

The <b>WDF_RETRIEVE_CHILD_FLAGS</b> enumeration defines flags that a driver can set before calling <a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistbeginiteration">WdfChildListBeginIteration</a>.

## -enum-fields

### -field WdfRetrieveUnspecified:0x0000

Reserved for internal use only.

### -field WdfRetrievePresentChildren:0x0001

Calls to <a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistretrievenextdevice">WdfChildListRetrieveNextDevice</a> will retrieve child devices for which a framework device object exists.

### -field WdfRetrieveMissingChildren:0x0002

Calls to <a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistretrievenextdevice">WdfChildListRetrieveNextDevice</a> will retrieve child devices that are marked as missing.

### -field WdfRetrievePendingChildren:0x0004

Calls to <a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistretrievenextdevice">WdfChildListRetrieveNextDevice</a> will retrieve child devices that the driver has reported as present, but for which a framework device object has not been created (because the framework has not called the driver's <a href="/windows-hardware/drivers/ddi/wdfchildlist/nc-wdfchildlist-evt_wdf_child_list_create_device">EvtChildListCreateDevice</a> callback function).

### -field WdfRetrieveAddedChildren:(WdfRetrievePresentChildren | WdfRetrievePendingChildren)

Calls to <a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistretrievenextdevice">WdfChildListRetrieveNextDevice</a> will retrieve child devices that are present or pending.

### -field WdfRetrieveAllChildren:(WdfRetrievePresentChildren | WdfRetrievePendingChildren | WdfRetrieveMissingChildren)

Calls to <a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistretrievenextdevice">WdfChildListRetrieveNextDevice</a> will retrieve child devices that are present, pending, or missing.

## -remarks

Before calling <a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistbeginiteration">WdfChildListBeginIteration</a>, your driver must set <b>WDF_RETRIEVE_CHILD_FLAGS</b>-typed flags in a <a href="/windows-hardware/drivers/ddi/wdfchildlist/ns-wdfchildlist-_wdf_child_list_iterator">WDF_CHILD_LIST_ITERATOR</a> structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdfchildlist/nc-wdfchildlist-evt_wdf_child_list_create_device">EvtChildListCreateDevice</a>



<a href="/windows-hardware/drivers/ddi/wdfchildlist/ns-wdfchildlist-_wdf_child_list_iterator">WDF_CHILD_LIST_ITERATOR</a>



<a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistbeginiteration">WdfChildListBeginIteration</a>



<a href="/windows-hardware/drivers/ddi/wdfchildlist/nf-wdfchildlist-wdfchildlistretrievenextdevice">WdfChildListRetrieveNextDevice</a>

