---
UID: NF:wdm.KdPrint
title: KdPrint macro (wdm.h)
description: The KdPrint macro sends a message to the kernel debugger.
tech.root: devtest
ms.date: 01/05/2023
keywords: ["KdPrint macro"]
ms.keywords: DebugFns_630aea64-3f51-4c73-8575-00a507846ab9.xml, KdPrint, KdPrint function [Driver Development Tools], devtest.kdprint, wdm/KdPrint
req.header: wdm.h
req.include-header: Wdm.h
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
req.lib: NtosKrnl.lib (See DbgPrint.)
req.dll: NtosKrnl.exe
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - KdPrint
 - wdm/KdPrint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - KdPrint
---

## -description

The **KdPrint** macro sends a message to the kernel debugger.

**KdPrint** sends a message only if the conditions you specify apply. More info in the section below.

A call to **KdPrint** requires double parentheses.

## -parameters

### -param _x_ [in]

Specifies a pointer to the format string to print. The _Format_ string supports most of the **printf**-style [format specification syntax](/cpp/c-runtime-library/format-specification-syntax-printf-and-wprintf-functions). However, the Unicode format codes (**%C**, **%S**, **%lc**, **%ls**, **%wc**, **%ws**, and **%wZ**) can only be used with IRQL = PASSIVE_LEVEL. The **KdPrint** routine does not support any of the floating point types (**%f**, **%e**, **%E**, **%g**, **%G**, **%a**, or **%A**).

## -remarks

**KdPrint** is identical to the **DbgPrint** routine in code that is compiled for a debug configuration.  This routine has no effect if compiled for a release configuration. Only kernel-mode drivers can call the **KdPrint** routine.

**KdPrint** sends a message only if certain conditions apply. Specifically, it behaves like [KdPrintEx](./nf-wdm-kdprintex.md) with the DEFAULT component and a message importance level of DPFLTR_INFO_LEVEL. In other words, the following two function calls are identical:

`KdPrint (( Format, arguments ))`

`KdPrintEx (( DPFLTR_DEFAULT_ID, DPFLTR_INFO_LEVEL, Format, arguments ))`

For more information about message filtering, components, and message importance level, see [Reading and Filtering Debugging Messages](/windows-hardware/drivers/devtest/reading-and-filtering-debugging-messages).

Regardless of which version of Windows you are using, it is recommended that you use **KdPrintEx** instead of **KdPrint**, since **KdPrintEx** allows you to control the conditions under which the message is sent.

Unless it is absolutely necessary, you should not obtain a string from user input or another process and pass it to **KdPrint**. If you do use a string that you did not create, you must verify that this is a valid format string, and that the format codes match the argument list in type and quantity. The best coding practice is for all _Format_ strings to be static and defined at compile time.

There is no upper limit to the size of the _Format_ string or the number of arguments. However, any single call to **KdPrint** will only transmit 512 bytes of information. There is also a limit to the size of the [DbgPrint](/windows-hardware/drivers/ddi/wdm/nf-wdm-dbgprint) buffer. See [The DbgPrint Buffer and the Debugger](/windows-hardware/drivers/devtest/reading-and-filtering-debugging-messages) for details.

## -see-also

[DbgPrint](./nf-wdm-dbgprint.md)

[DbgPrintEx](./nf-wdm-dbgprintex.md)

[KdPrintEx](./nf-wdm-kdprintex.md)
