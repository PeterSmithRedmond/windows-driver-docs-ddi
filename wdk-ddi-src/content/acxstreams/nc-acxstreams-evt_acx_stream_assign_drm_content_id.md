---
UID: NC:acxstreams.EVT_ACX_STREAM_ASSIGN_DRM_CONTENT_ID
tech.root: audio
title: EVT_ACX_STREAM_ASSIGN_DRM_CONTENT_ID
ms.date: 07/28/2022
targetos: Windows
description: The EVT_ACX_STREAM_ASSIGN_DRM_CONTENT_ID event tells the driver to assign a content ID for the purposes of DRM streaming.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: acxstreams.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - acxstreams.h
api_name:
 - EVT_ACX_STREAM_ASSIGN_DRM_CONTENT_ID
f1_keywords:
 - EVT_ACX_STREAM_ASSIGN_DRM_CONTENT_ID
 - acxstreams/EVT_ACX_STREAM_ASSIGN_DRM_CONTENT_ID
dev_langs:
 - c++
---

## -description

The **EVT_ACX_STREAM_ASSIGN_DRM_CONTENT_ID** event tells the driver to assign a content ID for the purposes of DRM streaming.

## -parameters

### -param Stream

An existing ACXSTREAM Object. For more information, see [ACX - Summary of ACX Objects](/windows-hardware/drivers/audio/acx-summary-of-objects).


### -param ContentId

Specifies a nonzero DRM content ID assigned to an ACX audio stream by [AcxDrmCreateContentMixed](nf-acxstreams-acxdrmcreatecontentmixed.md). Note that a content ID of zero represents an audio stream with default DRM content rights, and cannot be used with this function.

### -param DrmRights

Specifies the DRM content rights that are assigned to the stream that is identified by ContentId. This parameter is a pointer to a [ACXDRMRIGHTS structure](ns-acxstreams-acxdrmrights.md).

## -returns

Returns `STATUS_SUCCESS` if the call was successful. Otherwise, it returns an appropriate error code. For more information, see [Using NTSTATUS Values](/windows-hardware/drivers/kernel/using-ntstatus-values).

## -remarks

### Example

Example usage is shown below.

```cpp
    //
    // Init streaming callbacks.
    //
    ACX_STREAM_CALLBACKS_INIT(&streamCallbacks);
    ...
    streamCallbacks.EvtAcxStreamAssignDrmContentId = EvtStreamAssignDrmContentId;

    status = AcxStreamInitAssignAcxStreamCallbacks(StreamInit, &streamCallbacks);

...

_Use_decl_annotations_
PAGED_CODE_SEG
NTSTATUS
EvtStreamAssignDrmContentId(
    _In_ ACXSTREAM      Stream,
    _In_ ULONG          DrmContentId,
    _In_ PACXDRMRIGHTS  DrmRights
    )
{
    PSTREAM_CONTEXT ctx;

    PAGED_CODE();

    ctx = GetStreamContext(Stream);
    ASSERT(ctx);
    ASSERT(ctx->StreamEngine);

    return ctx->StreamEngine->AssignDrmContentId(DrmContentId, DrmRights);
}

```

### ACX requirements

**Minimum ACX version:** 1.0

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [ACXDRMRIGHTS structure](ns-acxstreams-acxdrmrights.md)
- [acxstreams.h header](index.md)
