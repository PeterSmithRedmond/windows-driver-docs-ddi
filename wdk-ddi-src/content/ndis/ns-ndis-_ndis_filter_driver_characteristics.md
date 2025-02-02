---
UID: NS:ndis._NDIS_FILTER_DRIVER_CHARACTERISTICS
title: _NDIS_FILTER_DRIVER_CHARACTERISTICS (ndis.h)
description: To specify its driver characteristics, a filter driver initializes an NDIS_FILTER_DRIVER_CHARACTERISTICS structure and passes it to NDIS.
old-location: netvista\ndis_filter_driver_characteristics.htm
tech.root: netvista
ms.date: 05/03/2019
keywords: ["NDIS_FILTER_DRIVER_CHARACTERISTICS structure"]
ms.keywords: "*PNDIS_FILTER_DRIVER_CHARACTERISTICS, NDIS_FILTER_DRIVER_CHARACTERISTICS, NDIS_FILTER_DRIVER_CHARACTERISTICS structure [Network Drivers Starting with Windows Vista], PNDIS_FILTER_DRIVER_CHARACTERISTICS, PNDIS_FILTER_DRIVER_CHARACTERISTICS structure pointer [Network Drivers Starting with Windows Vista], _NDIS_FILTER_DRIVER_CHARACTERISTICS, filter_structures_ref_8fc4ed95-82fe-47bd-849d-f9733647cacd.xml, ndis/NDIS_FILTER_DRIVER_CHARACTERISTICS, ndis/PNDIS_FILTER_DRIVER_CHARACTERISTICS, netvista.ndis_filter_driver_characteristics"
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
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
req.typenames: NDIS_FILTER_DRIVER_CHARACTERISTICS, *PNDIS_FILTER_DRIVER_CHARACTERISTICS
f1_keywords:
 - _NDIS_FILTER_DRIVER_CHARACTERISTICS
 - ndis/_NDIS_FILTER_DRIVER_CHARACTERISTICS
 - PNDIS_FILTER_DRIVER_CHARACTERISTICS
 - ndis/PNDIS_FILTER_DRIVER_CHARACTERISTICS
 - NDIS_FILTER_DRIVER_CHARACTERISTICS
 - ndis/NDIS_FILTER_DRIVER_CHARACTERISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndis.h
api_name:
 - _NDIS_FILTER_DRIVER_CHARACTERISTICS
 - PNDIS_FILTER_DRIVER_CHARACTERISTICS
 - NDIS_FILTER_DRIVER_CHARACTERISTICS
---

# _NDIS_FILTER_DRIVER_CHARACTERISTICS structure


## -description

To specify its driver characteristics, a filter driver initializes an
  NDIS_FILTER_DRIVER_CHARACTERISTICS structure and passes it to NDIS.

## -struct-fields

### -field Header

The 
     <a href="/windows-hardware/drivers/ddi/objectheader/ns-objectheader-ndis_object_header">NDIS_OBJECT_HEADER</a> structure for the
     filter driver characteristics structure (NDIS_FILTER_DRIVER_CHARACTERISTICS). Set the 
     <b>Type</b> member of the structure that 
     <b>Header</b> specifies to NDIS_OBJECT_TYPE_FILTER_DRIVER_CHARACTERISTICS.
     

To indicate the version of the NDIS_FILTER_DRIVER_CHARACTERISTICS structure, set the 
     <b>Revision</b> member to one of the following values:





#### NDIS_FILTER_CHARACTERISTICS_REVISION_3

Added the 
        <b>SynchronousOidRequestHandler</b> and <b>SynchronousOidRequestCompleteHandler</b> members for NDIS 6.80.

Set the 
        <b>Size</b> member to NDIS_SIZEOF_FILTER_DRIVER_CHARACTERISTICS_REVISION_3.



#### NDIS_FILTER_CHARACTERISTICS_REVISION_2

Added the 
        <b>DirectOidRequestHandler</b>, 
        <b>DirectOidRequestCompleteHandler</b>, and 
        <b>CancelDirectOidRequestHandler</b> members for NDIS 6.1.

Set the 
        <b>Size</b> member to NDIS_SIZEOF_FILTER_DRIVER_CHARACTERISTICS_REVISION_2.



#### NDIS_FILTER_CHARACTERISTICS_REVISION_1

Original version.

Set the 
        <b>Size</b> member to NDIS_SIZEOF_FILTER_DRIVER_CHARACTERISTICS_REVISION_1.

### -field MajorNdisVersion

The major version of NDIS that the driver is using. The current value is
     0x06.

### -field MinorNdisVersion

The minor NDIS version. The following are the available minor version value settings.

|Value|Meaning|
|--- |--- |
|0|NDIS 6|
|20|NDIS 6.20|
|30|NDIS 6.30|
|40|NDIS 6.40|
|50|NDIS 6.50|
|51|NDIS 6.51|
|60|NDIS 6.60|
|70|NDIS 6.70|
|80|NDIS 6.80|
|81|NDIS 6.81|
|82|NDIS 6.82|
|83|NDIS 6.83|
|84|NDIS 6.84|
|85|NDIS 6.85|
|86|NDIS 6.86|
|87|NDIS 6.87|
|88|NDIS 6.88|
|89|NDIS 6.89|

### -field MajorDriverVersion

Reserved for the major version number of the filter driver. Filter drivers can specify any value
     that they require.

### -field MinorDriverVersion

Reserved for the minor version number of the filter driver. Filter drivers can specify any value
     that they require.

### -field Flags

The following flag is supported in NDIS 6.89 and higher:

|Value|Meaning|
|--- |--- |
|NDIS_FILTER_DRIVER_UDP_RSC_NOT_SUPPORTED 0x00000008| The driver opt-outs of URO support. |

In NDIS 6.88 and below, **Flags** is reserved for NDIS. 

### -field FriendlyName

A Unicode string that represents the user-readable description of the filter driver.

### -field UniqueName

A Unicode string that represents the unique name for the filter driver. This string must be a GUID, enclosed in curly braces, for example "{5cbf81bd-5055-47cd-9055-a76b2b4e3697}". This GUID must match the one in the <b>NetCfgInstanceId</b> INF file entry in the filter driver's INF file. For more information, see <a href="/windows-hardware/drivers/network/inf-file-settings-for-filter-drivers">INF File Settings for Filter Drivers</a>.

### -field ServiceName

A Unicode string that represents the service name of the filter driver. This string must be the service name
     from the AddService directive in the filter driver's INF file. For more information, see <a href="/windows-hardware/drivers/network/inf-file-settings-for-filter-drivers">INF File Settings for Filter Drivers</a>.

### -field SetOptionsHandler

Specifies the entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-set_options">FilterSetOptions</a> function.

### -field SetFilterModuleOptionsHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_set_module_options">
     FilterSetModuleOptions</a> function.

### -field AttachHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_attach">FilterAttach</a> function.

### -field DetachHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_detach">FilterDetach</a> function.

### -field RestartHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_restart">FilterRestart</a> function.

### -field PauseHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_pause">FilterPause</a> function.

### -field SendNetBufferListsHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_send_net_buffer_lists">
     FilterSendNetBufferLists</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field SendNetBufferListsCompleteHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_send_net_buffer_lists_complete">
     FilterSendNetBufferListsComplete</a> function. To bypass this function, set this member to
     <b>NULL</b>.

### -field CancelSendNetBufferListsHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_cancel_send_net_buffer_lists">
     FilterCancelSendNetBufferLists</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field ReceiveNetBufferListsHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_receive_net_buffer_lists">
     FilterReceiveNetBufferLists</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field ReturnNetBufferListsHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_return_net_buffer_lists">
     FilterReturnNetBufferLists</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field OidRequestHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_oid_request">FilterOidRequest</a> function. To bypass
     this function, set this member to <b>NULL</b>.

### -field OidRequestCompleteHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_oid_request_complete">
     FilterOidRequestComplete</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field CancelOidRequestHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_cancel_oid_request">
     FilterCancelOidRequest</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field DevicePnPEventNotifyHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_device_pnp_event_notify">
     FilterDevicePnPEventNotify</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field NetPnPEventHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_net_pnp_event">FilterNetPnPEvent</a> function. To
     bypass this function, set this member to <b>NULL</b>.

### -field StatusHandler

The entry point of the caller's 
     <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_status">FilterStatus</a> function. To bypass this
     function, set this member to <b>NULL</b>.

### -field DirectOidRequestHandler

The entry point of the caller's 
      <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_direct_oid_request">
      FilterDirectOidRequest</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field DirectOidRequestCompleteHandler

The entry point of the caller's 
      <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_direct_oid_request_complete">
      FilterDirectOidRequestComplete</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field CancelDirectOidRequestHandler

The entry point of the caller's 
      <a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_cancel_direct_oid_request">
      FilterCancelDirectOidRequest</a> function. To bypass this function, set this member to <b>NULL</b>.

### -field SynchronousOidRequestHandler

The entry point of the caller's [*FilterSynchronousOidRequest*](nf-ndis-filter_synchronous_oid_request.md) function. To bypass this function, set this member to **NULL**.

### -field SynchronousOidRequestCompleteHandler

The entry point of the caller's [*FilterSynchronousOidRequestComplete*](nf-ndis-filter_synchronous_oid_request_complete.md) function. To bypass this function, set this member to **NULL**.

## -remarks

A filter driver calls the 
    <a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisfregisterfilterdriver">
    NdisFRegisterFilterDriver</a> function to register its characteristics, including the default entry
    points for its filter driver functions (<i>FilterXxx</i>). The filter driver initializes an NDIS_FILTER_DRIVER_CHARACTERISTICS structure and
    passes a pointer to this structure in the 
    <i>FilterCharacteristics</i> parameter of 
    <b>NdisFRegisterFilterDriver</b>.

## -see-also

<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_attach">FilterAttach</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_cancel_direct_oid_request">
   FilterCancelDirectOidRequest</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_cancel_oid_request">FilterCancelOidRequest</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_cancel_send_net_buffer_lists">
   FilterCancelSendNetBufferLists</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_detach">FilterDetach</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_device_pnp_event_notify">FilterDevicePnPEventNotify</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_direct_oid_request">FilterDirectOidRequest</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_direct_oid_request_complete">
   FilterDirectOidRequestComplete</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_net_pnp_event">FilterNetPnPEvent</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_oid_request">FilterOidRequest</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_oid_request_complete">FilterOidRequestComplete</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_pause">FilterPause</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_receive_net_buffer_lists">FilterReceiveNetBufferLists</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_restart">FilterRestart</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_return_net_buffer_lists">FilterReturnNetBufferLists</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_send_net_buffer_lists">FilterSendNetBufferLists</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_send_net_buffer_lists_complete">
   FilterSendNetBufferListsComplete</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_set_module_options">FilterSetModuleOptions</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-set_options">FilterSetOptions</a>



<a href="/windows-hardware/drivers/ddi/ndis/nc-ndis-filter_status">FilterStatus</a>



<a href="/windows-hardware/drivers/network/inf-file-settings-for-filter-drivers">INF File Settings for Filter Drivers</a>



<a href="/windows-hardware/drivers/network/initializing-a-filter-driver">Initializing a Filter Driver</a>



<a href="/windows-hardware/drivers/ddi/ndis/ns-ndis-_ndis_filter_partial_characteristics">
   NDIS_FILTER_PARTIAL_CHARACTERISTICS</a>



<a href="/windows-hardware/drivers/ddi/objectheader/ns-objectheader-ndis_object_header">NDIS_OBJECT_HEADER</a>



<a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisfregisterfilterdriver">NdisFRegisterFilterDriver</a>

