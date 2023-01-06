---
UID: NE:acxstreams._ACX_STREAM_STATE
tech.root: audio
title: ACX_STREAM_STATE
ms.date: 07/28/2022
targetos: Windows
description: ACX_STREAM_STATE describes the Acx Stream State flags. This function is located in the acxstreams header.
prerelease: true
req.construct-type: enumeration
req.ddi-compliance: 
req.header: acxstreams.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - acxstreams.h
api_name:
 - _ACX_STREAM_STATE
 - PACX_STREAM_STATE
 - ACX_STREAM_STATE
f1_keywords:
 - _ACX_STREAM_STATE
 - acxstreams/_ACX_STREAM_STATE
 - PACX_STREAM_STATE
 - acxstreams/PACX_STREAM_STATE
 - ACX_STREAM_STATE
 - acxstreams/ACX_STREAM_STATE
dev_langs:
 - c++
---

## -description

**ACX_STREAM_STATE** describes the Acx Stream State flags.

## -enum-fields

### -field AcxStreamStateStop

Describes the Acx Stream State is stopped.

### -field AcxStreamStateAcquire

Describes the Acx Stream State is being acquired. This state is only used internally; the stream will transition directly from AcxStreamStateStop to AcxStreamStatePause or from AcxStreamStatePause to AcxStreamStateStop.

### -field AcxStreamStatePause

Describes the Acx Stream State as paused.

### -field AcxStreamStateRun

Describes the Acx Stream State as running.

### -field AcxStreamStateMaximum

Describes the Acx Stream State Maximum. This value is used for internal validation.

## -remarks

An AcxStream support different states. These states indicate when audio is flowing (RUN state) or not flowing (PAUSE or STOP state).

Once the stream is created and the appropriate buffers are allocated, the stream is in the Pause state awaiting stream start. When the client puts the stream into Play state, the ACX framework will call all circuits associated with the stream to indicate the stream state is in Play. The ACXPIN will then be placed in the Play state, at which point data will start flowing.

Once the stream is created and the resources are allocated, the application will call Start on the stream to start playback.

The client starts by pre-rolling a buffer. When the client calls ReleaseBuffer, this will translate to a call in AudioKSE that will call into the ACX layer, which will call EvtAcxStreamSetRenderPacket on the active ACXSTREAM. The property will include the packet index (0-based) and, if appropriate, an EOS flag with the byte offset of the end of the stream in the current packet.

During ACX device power down and removal, if streams are present, ACX SetState callbacks are invoked to transition all circuit's streams to Pause. This is Stream Instance scoped.

- After AcxStreamCreate, the AcxStream is in the AcxStreamStateStop state.
- After EvtAcxStreamPrepareHardware returns successfully the AcxStream will be in the AcxStreamStatePause state.
- After EvtAcxStreamRun returns successfully the AcxStream will be in the AcxStreamStateRun state.
- After EvtAcxStreamPause returns the AcxStream will be in the AcxStreamStatePause state.
- After EvtAcxReleaseHardware returns the AcxStream will be in the AcxStreamStop state.

### Example

Example usage is shown below.

```cpp
    ACX_STREAM_STATE    m_CurrentState;
...
    if (m_CurrentState != AcxStreamStatePause)
    {
        status = STATUS_INVALID_STATE_TRANSITION;
        return status;
    }
```

### ACX requirements

**Minimum ACX version:** 1.0

For more information about ACX versions, see [ACX version overview](/windows-hardware/drivers/audio/acx-version-overview).

## -see-also

- [acxstreams.h header](index.md)
