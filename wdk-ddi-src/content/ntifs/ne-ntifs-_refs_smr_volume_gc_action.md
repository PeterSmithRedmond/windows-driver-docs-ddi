---
UID: NE:ntifs._REFS_SMR_VOLUME_GC_ACTION
title: REFS_SMR_VOLUME_GC_ACTION (ntifs.h)
description: Learn more about the REFS_SMR_VOLUME_GC_ACTION enumeration.
tech.root: ifsk
ms.date: 07/06/2023
keywords: ["REFS_SMR_VOLUME_GC_ACTION enumeration"]
ms.keywords: "*PREFS_SMR_VOLUME_GC_ACTION, PREFS_SMR_VOLUME_GC_ACTION, REFS_SMR_VOLUME_GC_ACTION, SmrGcActionPause, SmrGcActionStart, SmrGcActionStartFullSpeed, SmrGcActionStop, _REFS_SMR_VOLUME_GC_ACTION, ifsk.refs_smr_volume_gc_action, ntifs/PREFS_SMR_VOLUME_GC_ACTION, ntifs/REFS_SMR_VOLUME_GC_ACTION, ntifs/SmrGcActionPause, ntifs/SmrGcActionStart, ntifs/SmrGcActionStartFullSpeed, ntifs/SmrGcActionStop"
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
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
req.typenames: REFS_SMR_VOLUME_GC_ACTION, *PREFS_SMR_VOLUME_GC_ACTION
f1_keywords:
 - _REFS_SMR_VOLUME_GC_ACTION
 - ntifs/_REFS_SMR_VOLUME_GC_ACTION
 - PREFS_SMR_VOLUME_GC_ACTION
 - ntifs/PREFS_SMR_VOLUME_GC_ACTION
 - REFS_SMR_VOLUME_GC_ACTION
 - ntifs/REFS_SMR_VOLUME_GC_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntifs.h
api_name:
 - _REFS_SMR_VOLUME_GC_ACTION
 - PREFS_SMR_VOLUME_GC_ACTION
 - REFS_SMR_VOLUME_GC_ACTION
---

# REFS_SMR_VOLUME_GC_ACTION enumeration

## -description

The **REFS_SMR_VOLUME_GC_ACTION** enum contains the available garbage collection commands for [**FSCTL_SET_REFS_SMR_VOLUME_GC_PARAMETERS**](/windows-hardware/drivers/ifs/fsctl-set-refs-smr-volume-gc-parameters).

## -enum-fields

### -field SmrGcActionStart:1

Specifies to start garbage collection or resume from a previously paused garbage collection. By default, garbage collection is off on Shingled Magnetic Recording (SMR) volumes.  Only users with admin rights can modify this setting.

### -field SmrGcActionStartFullSpeed:2

Specifies to start or resume garbage collection at full speed, issuing Read/Write I/O up to one SMR band size (256mb) at a time.

### -field SmrGcActionPause:3

Specifies to temporarily stop the garbage collection if it's in progress.  If the garbage collection is not in progress, there will be no operation.

### -field SmrGcActionStop:4

Specifies to stop the garbage collection process and removes the ability to resume.  If garbage collection was paused previously, this will clear the ability to resume from the point of the pause.

## -see-also

[**FSCTL_SET_REFS_SMR_VOLUME_GC_PARAMETERS**](/windows-hardware/drivers/ifs/fsctl-set-refs-smr-volume-gc-parameters)
