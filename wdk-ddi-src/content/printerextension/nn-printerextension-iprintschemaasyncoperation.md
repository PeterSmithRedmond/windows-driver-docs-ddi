---
UID: NN:printerextension.IPrintSchemaAsyncOperation
title: IPrintSchemaAsyncOperation (printerextension.h)
description: Represents an asynchronous operation context for validation, merge or commit operations.
tech.root: print
ms.date: 01/04/2023
keywords: ["IPrintSchemaAsyncOperation interface"]
ms.keywords: IPrintSchemaAsyncOperation, IPrintSchemaAsyncOperation interface [Print Devices], IPrintSchemaAsyncOperation interface [Print Devices],described, print.iprintschemaasyncoperation_interface, printerextension/IPrintSchemaAsyncOperation
req.header: printerextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - IPrintSchemaAsyncOperation
 - printerextension/IPrintSchemaAsyncOperation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Printerextension.h
api_name:
 - IPrintSchemaAsyncOperation
---

## -description

Represents an asynchronous operation context for validation, merge or commit operations.

## -remarks

Any event sink that implements [IPrintSchemaAsyncOperationEvent](./nn-printerextension-iprintschemaasyncoperationevent.md) is connected to the associated event source, **IPrintSchemaAsyncOperation**, via the [IConnectionPoint](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) mechanism. You must retrieve a pointer to the **IConnectionPoint** interface by invoking **QueryInterface** on the **IPrinterQueue** object.

It is mandatory to implement **IDispatch::Invoke** on the event sink that implements **IPrinterQueueEvent**, since that is the mechanism via which events are raised. It is sufficient to provide stub implementations of the other methods on the **IDispatch** interface.

## -see-also

[IConnectionPoint](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)

[IPrintSchemaAsyncOperationEvent](./nn-printerextension-iprintschemaasyncoperationevent.md)
