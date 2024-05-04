---
UID: NE:d3d12umddi.D3D12DDI_STATE_OBJECT_TYPE
title: D3D12DDI_STATE_OBJECT_TYPE (d3d12umddi.h)
description: Learn more about the D3D12DDI_STATE_OBJECT_TYPE enumeration.
ms.date: 05/03/2024
keywords: ["D3D12DDI_STATE_OBJECT_TYPE enumeration"]
ms.keywords: D3D12DDI_STATE_OBJECT_TYPE, D3D12DDI_STATE_OBJECT_TYPE,
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1809
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12DDI_STATE_OBJECT_TYPE
targetos: Windows
tech.root: display
ms.custom: RS5
f1_keywords:
 - D3D12DDI_STATE_OBJECT_TYPE
 - d3d12umddi/D3D12DDI_STATE_OBJECT_TYPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12umddi.h
api_name:
 - D3D12DDI_STATE_OBJECT_TYPE
dev_langs:
 - c++
---

# D3D12DDI_STATE_OBJECT_TYPE enumeration

## -description

The **D3D12DDI_STATE_OBJECT_TYPE** enumeration defines the types of state objects that can be created.

## -enum-fields

### -field D3D12DDI_STATE_OBJECT_TYPE_COLLECTION

A collection can contain any amount of subobjects, but doesn’t have constraints. Not all dependencies that the included subobjects have must be resolved in the same collection  Even if dependencies are locally defined, the set of subobjects doesn’t have to be the complete set of state that will eventually be used on the GPU. For instance, a collection may not include all shaders needed to *raytrace* a scene, though it could.

The purpose of a collection is to allow an application to pass an arbitrarily large or small collection of state to drivers to compile at once (e.g. on a given thread).

### -field D3D12DDI_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE

An RTPSO (ray tracing pipeline state object) represents a full set of shaders that could be reachable by a DispatchRays() call, with all configuration options resolved, such as local root signatures and other state.  

An RTPSO can be thought of as an *executable* state object.

### -field D3D12DDI_STATE_OBJECT_TYPE_EXECUTABLE

This state object type refers to a fully configured and executable pipeline state that can be used for rendering or compute operations.

## -remarks

State objects are used to encapsulate a set of states that configure the graphics pipeline for rendering or compute operations, including those for ray tracing.

State objects have a type that dictates rules about the subobjects they contain and how the state objects can be used.

## -see-also

[**D3D12DDI_STATE_SUBOBJECT_TYPE**](ne-d3d12umddi-d3d12ddi_state_subobject_type.md)

[**PFND3D12DDI_CREATE_STATE_OBJECT_0054**](nc-d3d12umddi-pfnd3d12ddi_create_state_object_0054.md)
