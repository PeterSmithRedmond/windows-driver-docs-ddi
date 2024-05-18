---
UID: NS:d3dkmdt._DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
title: _DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS (d3dkmdt.h)
description: The DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS structure contains parameters to set the version of a High-bandwidth Digital Content Protection (HDCP) System Renewability Message (SRM) for a protected output.
old-location: display\dxgkmdt_opm_set_hdcp_srm_parameters.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS structure"]
ms.keywords: DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS, DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS structure [Display Devices], DmStructs_6e80579a-8a17-47c0-b877-1e7712de2f04.xml, _DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS, d3dkmdt/DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS, display.dxgkmdt_opm_set_hdcp_srm_parameters
req.header: d3dkmdt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.typenames: DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
f1_keywords:
 - _DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
 - d3dkmdt/_DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
 - DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
 - d3dkmdt/DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmdt.h
api_name:
 - _DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
 - DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS
---

# _DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS structure


## -description

The DXGKMDT_OPM_SET_HDCP_SRM_PARAMETERS structure contains parameters to set the version of a High-bandwidth Digital Content Protection (HDCP) System Renewability Message (SRM) for a protected output.

## -struct-fields

### -field ulSRMVersion

The version number of an HDCP SRM. The least significant bits (bits 0 through 15) contain the SRM's version number in little-endian format. The SRM's version number is stored in the SRM's SRM version field in little-endian format. For more information about the SRM's SRM version field, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=38728">HDCP Specification Revision 1.1</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_configure_parameters">DXGKMDT_OPM_CONFIGURE_PARAMETERS</a>



<a href="/windows-hardware/drivers/ddi/dispmprt/nc-dispmprt-dxgkddi_opm_configure_protected_output">DxgkDdiOPMConfigureProtectedOutput</a>

