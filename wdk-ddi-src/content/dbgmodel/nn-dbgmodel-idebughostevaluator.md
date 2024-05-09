---
UID: NN:dbgmodel.IDebugHostEvaluator
title: IDebugHostEvaluator (dbgmodel.h)
description: The IDebugHostEvaluator (dbgmodel.h) interface provides access to the language based expression evaluator in the underlying debugger.
ms.date: 07/13/2018
keywords: ["IDebugHostEvaluator interface"]
req.header: dbgmodel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: debugger
ms.custom: RS5
f1_keywords:
 - IDebugHostEvaluator
 - dbgmodel/IDebugHostEvaluator
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dbgmodel.h
api_name:
 - IDebugHostEvaluator
---

# IDebugHostEvaluator interface


## -description

The expression evaluator interface to the underlying debugger.

## -inheritance

IDebugHostEvaluator inherits from IUnknown.

## -remarks

One of the most important pieces of functionality which the debug host provides to clients is access to its language based expression evaluator. The IDebugHostEvaluator and [IDebugHostEvaluator2](nn-dbgmodel-idebughostevaluator2.md) interfaces are the means to access that functionality from the debug host.

## -see-also

[Debugger Data Model C++ Overview](/windows-hardware/drivers/debugger/data-model-cpp-overview)
