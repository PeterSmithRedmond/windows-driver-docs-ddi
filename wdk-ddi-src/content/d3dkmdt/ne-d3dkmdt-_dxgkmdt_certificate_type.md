---
UID: NE:d3dkmdt._DXGKMDT_CERTIFICATE_TYPE
title: DXGKMDT_CERTIFICATE_TYPE (d3dkmdt.h)
description: The DXGKMDT_CERTIFICATE_TYPE enumeration identifies the type of certificate that callers of the DxgkDdiOPMGetCertificateSize and DxgkDdiOPMGetCertificate functions require.
old-location: display\dxgkmdt_certificate_type.htm
tech.root: display
ms.date: 03/14/2023
keywords: ["DXGKMDT_CERTIFICATE_TYPE enumeration"]
ms.keywords: DXGKMDT_CERTIFICATE_TYPE, DXGKMDT_CERTIFICATE_TYPE enumeration [Display Devices], DXGKMDT_COPP_CERTIFICATE, DXGKMDT_FORCE_ULONG, DXGKMDT_OPM_CERTIFICATE, DXGKMDT_UAB_CERTIFICATE, DmEnums_837195ed-375e-43ef-a854-1d1f0aab0c84.xml, _DXGKMDT_CERTIFICATE_TYPE, d3dkmdt/DXGKMDT_CERTIFICATE_TYPE, d3dkmdt/DXGKMDT_COPP_CERTIFICATE, d3dkmdt/DXGKMDT_FORCE_ULONG, d3dkmdt/DXGKMDT_OPM_CERTIFICATE, d3dkmdt/DXGKMDT_UAB_CERTIFICATE, display.dxgkmdt_certificate_type
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
req.typenames: DXGKMDT_CERTIFICATE_TYPE
f1_keywords:
 - _DXGKMDT_CERTIFICATE_TYPE
 - d3dkmdt/_DXGKMDT_CERTIFICATE_TYPE
 - DXGKMDT_CERTIFICATE_TYPE
 - d3dkmdt/DXGKMDT_CERTIFICATE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmdt.h
api_name:
 - _DXGKMDT_CERTIFICATE_TYPE
 - DXGKMDT_CERTIFICATE_TYPE
---

# DXGKMDT_CERTIFICATE_TYPE enumeration

## -description

The **DXGKMDT_CERTIFICATE_TYPE** enumeration identifies the type of certificate that callers of the [**DxgkDdiOPMGetCertificateSize**](../dispmprt/nc-dispmprt-dxgkddi_opm_get_certificate_size.md) and [**DxgkDdiOPMGetCertificate**](../dispmprt/nc-dispmprt-dxgkddi_opm_get_certificate.md) functions require.

## -enum-fields

### -field DXGKMDT_OPM_CERTIFICATE

Indicates an Output Protection Management (OPM) certificate.

### -field DXGKMDT_COPP_CERTIFICATE

Indicates a Certified Output Protection Protocol (COPP) certificate.

### -field DXGKMDT_UAB_CERTIFICATE

Indicates a User Accessible Bus (UAB) certificate.

### -field DXGKMDT_INDIRECT_DISPLAY_CERTIFICATE

### -field DXGKMDT_FORCE_ULONG

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

## -remarks

For more information about certificates that are used with OPM, download the [Output Content Protection and Windows Vista](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F5%2FD%2F6%2F5D6EAF2B-7DDF-476B-93DC-7CF0072878E6%2Foutput_protect.doc%3Fwww.dailytech.com&wdOrigin=BROWSELINK) document.

## -see-also

[**DxgkDdiOPMGetCertificate**](../dispmprt/nc-dispmprt-dxgkddi_opm_get_certificate.md)

[**DxgkDdiOPMGetCertificateSize**](../dispmprt/nc-dispmprt-dxgkddi_opm_get_certificate_size.md)
