---
UID: NF:ntifs.PoRegisterSystemState
title: PoRegisterSystemState function (ntifs.h)
description: Learn more about the PoRegisterSystemState routine.
tech.root: kernel
ms.date: 07/06/2023
keywords: ["PoRegisterSystemState function"]
ms.keywords: PoRegisterSystemState, PoRegisterSystemState routine [Kernel-Mode Driver Architecture], kernel.poregistersystemstate, portn_477a2d72-00f7-45a1-b7ca-504b741c5fe0.xml, wdm/PoRegisterSystemState
req.header: ntifs.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Windows 2000
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: <=APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - PoRegisterSystemState
 - ntifs/PoRegisterSystemState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - PoRegisterSystemState
---

# PoRegisterSystemState function (ntifs.h)

## -description

The **PoRegisterSystemState** routine registers the system as busy due to certain activity.

## -parameters

### -param StateHandle [in, out]

A pointer to a caller-supplied buffer for a registration state handle. The size, in bytes, of the buffer is ```sizeof(ULONG)```. If NULL, this is a new registration. If non-NULL, this parameter points to a handle that was returned by a previous call to **PoRegisterSystemState**.

### -param Flags [in]

Indicates the type of activity, as specified by a bitwise OR of one or more of the following values:

| Value | Meaning |
| ----- | ------- |
| ES_SYSTEM_REQUIRED  | The system is not idle, regardless of apparent load. |
| ES_DISPLAY_REQUIRED | Use of the display is required. |
| ES_USER_PRESENT     | A user is present. |
| ES_CONTINUOUS       | The settings are continuous and should remain in effect until explicitly changed. |

## -returns

**PoRegisterSystemState** returns a handle to be used later to change or unregister the system busy state. It returns NULL if the handle could not be allocated.

## -remarks

**PoRegisterSystemState** registers the system busy state as indicated by the flags. The registration persists until the caller explicitly changes it with another call to **PoRegisterSystemState** or cancels it with a call to [**PoUnregisterSystemState**](nf-ntifs-pounregistersystemstate.md).

The **Flags** parameter specifies the type of activity in progress. Drivers can specify any combination of the flags.

Setting ES_CONTINUOUS makes the busy state persist until a driver explicitly changes or cancels it by calling **PoRegisterSystemState** or **PoUnregisterSystemState**.

A driver can set the system busy state to request that the [power manager](/windows-hardware/drivers/kernel/power-manager) avoid system power state transitions out of the system working state (S0) while driver activity is occurring. Note, however, that under some circumstances (such as a critically low battery) the power manager may override this request and put the system to sleep anyway.

To set the system power state, call [**PoSetSystemState**](../wdm/nf-wdm-posetsystemstate.md).

## -see-also

[**PoSetSystemState**](../wdm/nf-wdm-posetsystemstate.md)

[**PoUnregisterSystemState**](nf-ntifs-pounregistersystemstate.md)
