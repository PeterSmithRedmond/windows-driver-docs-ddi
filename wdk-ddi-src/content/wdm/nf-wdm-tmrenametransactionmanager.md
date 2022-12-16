---
UID: NF:wdm.TmRenameTransactionManager
title: TmRenameTransactionManager function (wdm.h)
description: The TmRenameTransactionManager routine changes the identity of the transaction manager object that is stored in the CLFS log file stream contained in the log file name.
tech.root: kernel
ms.date: 12/13/2022
keywords: ["TmRenameTransactionManager function"]
ms.keywords: TmRenameTransactionManager, TmRenameTransactionManager , TmRenameTransactionManager routine [Kernel-Mode Driver Architecture], kernel.tmrenametransactionmanager_, wdm/TmRenameTransactionManager
req.header: wdm.h
req.include-header: 
req.target-type: Universal
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
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - TmRenameTransactionManager
 - wdm/TmRenameTransactionManager
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdm.h
 - Ext-MS-Win-ntos-tm-l1-1-0.dll
 - tm.sys
api_name:
 - TmRenameTransactionManager
---

## -description

The **TmRenameTransactionManager** routine changes the identity of the transaction manager object that is stored in the [CLFS](/windows-hardware/drivers/kernel/windows-kernel-mode-clfs-library) log file stream contained in the log file name.

> [!WARNING]
> Changing the identity of the transaction manger object might break any cross-log transactional links that may exist.

## -parameters

### -param LogFileName [in]

A pointer to a [UNICODE_STRING](/windows/win32/api/ntdef/ns-ntdef-_unicode_string) structure that contains the path and file name of a [CLFS](/windows-hardware/drivers/kernel/windows-kernel-mode-clfs-library) log file stream to be associated with the transaction manager object.

### -param ExistingTransactionManagerGuid [in]

A pointer to a GUID structure that represents the current name of the transaction manager object.

## -returns

The **TmRenameTransactionManager** routine returns an NTSTATUS value. If the routine fails, it returns an error code.
