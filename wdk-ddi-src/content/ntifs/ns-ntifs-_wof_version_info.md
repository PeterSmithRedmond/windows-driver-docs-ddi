---
UID: NS:ntifs._WOF_VERSION_INFO
title: WOF_VERSION_INFO (ntifs.h)
description: Learn more about the WOF_VERSION_INFO structure.
tech.root: ifsk
ms.date: 07/06/2023
keywords: ["WOF_VERSION_INFO structure"]
ms.keywords: "*PWOF_VERSION_INFO, PWOF_VERSION_INFO, PWOF_VERSION_INFO structure pointer [Installable File System Drivers], WOF_VERSION_INFO, WOF_VERSION_INFO structure [Installable File System Drivers], _WOF_VERSION_INFO, ifsk.wof_version_info, ntifs/PWOF_VERSION_INFO, ntifs/WOF_VERSION_INFO"
req.header: ntifs.h
req.include-header: Ntifs.h, Fltkernel.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
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
req.typenames: WOF_VERSION_INFO, *PWOF_VERSION_INFO
f1_keywords:
 - _WOF_VERSION_INFO
 - ntifs/_WOF_VERSION_INFO
 - PWOF_VERSION_INFO
 - ntifs/PWOF_VERSION_INFO
 - WOF_VERSION_INFO
 - ntifs/WOF_VERSION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntifs.h
api_name:
 - _WOF_VERSION_INFO
 - PWOF_VERSION_INFO
 - WOF_VERSION_INFO
---

# WOF_VERSION_INFO structure

## -description

The **WOF_VERSION_INFO** structure contains the version corresponding to the driver supporting a given provider.

## -struct-fields

### -field WofVersion

The version of the WOF driver. This value includes the major and minor version numbers of the operating system in the high-order word, and the build number of the operating system in the low-order word. The major version can be extracted with HIBYTE(HIWORD(**WofVersion**)); the minor version can be extracted with LOBYTE(HIWORD(**WofVersion**)); the build number can be extracted with LOWORD(**WofVersion**).

## -see-also

[**FSCTL_GET_WOF_VERSION**](/windows-hardware/drivers/ifs/fsctl-get-wof-version)

[**WOF_EXTERNAL_FILE_ID**](ns-ntifs-_wof_external_file_id.md)

[**WOF_EXTERNAL_INFO**](ns-ntifs-_wof_external_info.md)
