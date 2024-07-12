---
UID: NF:fwpmk.FwpmProviderContextGetById2
tech.root: netvista
title: FwpmProviderContextGetById2
ms.date: 06/13/2024
targetos: Windows
description: The FwpmProviderContextGetById2 function retrieves a provider context.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fwpmk.h
req.idl: 
req.include-header: 
req.irql: <= PASSIVE_LEVEL
req.kmdf-ver: 
req.lib: fwpkclnt.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Available starting with Windows Vista.
req.target-min-winversvr: 
req.target-type: Universal
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpmk.h
api_name:
 - FwpmProviderContextGetById2
f1_keywords:
 - FwpmProviderContextGetById2
 - fwpmk/FwpmProviderContextGetById2
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmProviderContextGetById2
---

## -description

The **FwpmProviderContextGetById2** function retrieves a provider context.

## -parameters

### -param engineHandle [in]

Handle for an open session to the filter engine. Call **[FwpmEngineOpen0](nf-fwpmk-fwpmengineopen0.md)** to open a session to the filter engine.

### -param id [in]

A run-time identifier for the desired object. This must be the run-time identifier that was received from the system when the application called **[FwpmProviderContextAdd2](nf-fwpmk-fwpmprovidercontextadd2.md)** for this object.

### -param providerContext [out]

The provider context information.

## -returns

| Return code/value | Description |
|---|---|
| **ERROR_SUCCESS**<br>0 | The provider context was retrieved successfully. |
| **FWP_E_\* error code**<br>0x80320001—0x80320039 | A Windows Filtering Platform (WFP) specific error. See [WFP Error Codes](/windows/win32/fwp/wfp-error-codes) for details. |
| **RPC_\* error code**<br>0x80010001—0x80010122 | Failure to communicate with the remote or local firewall engine. |
| **Other NTSTATUS codes** | An error occurred. |

## -remarks

The caller must free the returned object by a call to **[FwpmFreeMemory0](nf-fwpmk-fwpmfreememory0.md)**.

The caller needs [FWPM_ACTRL_READ](/windows/desktop/FWP/access-right-identifiers) access to the provider context. See [Access Control](/windows/desktop/FWP/access-control) for more information.

**FwpmProviderContextGetById1** is a specific implementation of **FwpmProviderContextGetById**. See [WFP Version-Independent Names and Targeting Specific Versions of Windows](/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows) for more information.

## -see-also

- **[FwpmEngineOpen0](nf-fwpmk-fwpmengineopen0.md)**
- **[FwpmProviderContextAdd2](nf-fwpmk-fwpmprovidercontextadd2.md)**
- **[FwpmFreeMemory0](nf-fwpmk-fwpmfreememory0.md)**
- [FWPM_PROVIDER_CONTEXT2](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
- [WFP Error Codes](/windows/win32/fwp/wfp-error-codes)
- [FWPM_ACTRL_READ](/windows/desktop/FWP/access-right-identifiers)
- [Access Control](/windows/desktop/FWP/access-control)
- [WFP Version-Independent Names and Targeting Specific Versions of Windows](/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows)