---
UID: NC:d3dkmddi.DXGKDDI_SUSPENDCONTEXT
title: DXGKDDI_SUSPENDCONTEXT (d3dkmddi.h)
description: Learn more about the DXGKDDI_SUSPENDCONTEXT callback function.
ms.date: 04/08/2024
keywords: ["DXGKDDI_SUSPENDCONTEXT callback function"]
req.header: d3dkmddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: display
ms.custom: RS5
f1_keywords:
 - DXGKDDI_SUSPENDCONTEXT
 - d3dkmddi/DXGKDDI_SUSPENDCONTEXT
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3dkmddi.h
api_name:
 - DXGKDDI_SUSPENDCONTEXT
dev_langs:
 - c++
---

# DXGKDDI_SUSPENDCONTEXT callback function

## -description

**DxgkddiSuspendContext** instructs the GPU to suspend a context. If the GPU doesn’t acknowledge the suspend completion within the TDR (timeout detection and recovery) timeout, the OS will detect the engine timeout and perform an engine reset.

## -parameters

### -param hAdapter

[in] The hardware context to be preempted and marked as suspended. This type of preemption request doesn't have a grace period, and is expected to be honored by the GPU as soon as possible.

### -param pSuspendContext

[in] Pointer to a [**DXGKARG_SUSPENDCONTEXT**](ns-d3dkmddi-_dxgkarg_suspendcontext.md) structure that contains additional arguments for this function.

## -returns

**DxgkddiSuspendContext** returns STATUS_SUCCESS if the context is already suspended at the time of this call. Otherwise, this value is set to STATUS_PENDING, and the suspend operation will be finished when **contextSuspendFence** is signaled via an interrupt.

## -remarks

Register your implementation of this callback function by setting it in [**DRIVER_INITIALIZATION_DATA**](/windows-hardware/drivers/ddi/dispmprt/ns-dispmprt-_driver_initialization_data).

Even though the round robin preemption can be initiated by the GPU, the OS still needs a way to preempt the context for other reasons; for example, if it needs to move its allocations around or perform a GPU power transition.

The context suspend value is necessary to handle cases when the OS suspends a context, doesn’t wait for the suspend acknowledgment, resumes, and suspends a context again. The suspend value will allow the OS to distinguish between the previous suspend acknowledgement and the latest one.

Once a context is suspended, it is assumed that all references to it are gone from the GPU, and the OS is free to destroy the context or move its memory around. Unlike WDDM 2.3 or earlier, no separate NULL context switch command (previously indicated by the **ContextSwitch** flag in **DxgkDdiSubmitCommandVirtual**) is present in WDDM 2.4 scheduling mode, because **DxgkddiSuspendContext** is supposed to do this work.

## -see-also

[**DxgkddiResumeContext**](nc-d3dkmddi-dxgkddi_resumecontext.md)

[**DXGKARG_SUSPENDCONTEXT**](ns-d3dkmddi-_dxgkarg_suspendcontext.md)
