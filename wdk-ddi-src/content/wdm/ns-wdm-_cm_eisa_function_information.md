---
UID: NS:wdm._CM_EISA_FUNCTION_INFORMATION
title: _CM_EISA_FUNCTION_INFORMATION (wdm.h)
description: The _CM_EISA_FUNCTION_INFORMATION structure (wdm.h)  defines detailed EISA configuration information returned by HalGetBusData or HalGetBusDataByOffset.
tech.root: kernel
ms.date: 01/18/2023
keywords: ["CM_EISA_FUNCTION_INFORMATION structure"]
ms.keywords: "*PCM_EISA_FUNCTION_INFORMATION, CM_EISA_FUNCTION_INFORMATION, CM_EISA_FUNCTION_INFORMATION structure [Kernel-Mode Driver Architecture], PCM_EISA_FUNCTION_INFORMATION, PCM_EISA_FUNCTION_INFORMATION structure pointer [Kernel-Mode Driver Architecture], _CM_EISA_FUNCTION_INFORMATION, kernel.cm_eisa_function_information, kstruct_a_0ecf5914-f26d-415f-b410-ff2f131b2b08.xml, wdm/CM_EISA_FUNCTION_INFORMATION, wdm/PCM_EISA_FUNCTION_INFORMATION"
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
req.target-type: Windows
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
req.irql: 
targetos: Windows
req.typenames: CM_EISA_FUNCTION_INFORMATION, *PCM_EISA_FUNCTION_INFORMATION
f1_keywords:
 - _CM_EISA_FUNCTION_INFORMATION
 - wdm/_CM_EISA_FUNCTION_INFORMATION
 - PCM_EISA_FUNCTION_INFORMATION
 - wdm/PCM_EISA_FUNCTION_INFORMATION
 - CM_EISA_FUNCTION_INFORMATION
 - wdm/CM_EISA_FUNCTION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - _CM_EISA_FUNCTION_INFORMATION
 - PCM_EISA_FUNCTION_INFORMATION
 - CM_EISA_FUNCTION_INFORMATION
---

## -description

The **CM_EISA_FUNCTION_INFORMATION** structure defines detailed EISA configuration information returned by [HalGetBusData](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85)) for the input *BusDataType ***EisaConfiguration**, or by **HalGetBusDataByOffset** for the input *BusDataType ***EisaConfiguration** and the *Offset* zero, assuming the caller-allocated *Buffer* is of sufficient *Length*.

## -struct-fields

### -field CompressedId

The EISA compressed identification of the device at this slot. The value is identical to the **CompressedId** member of the [CM_EISA_SLOT_INFORMATION](/windows-hardware/drivers/ddi/wdm/ns-wdm-_cm_eisa_slot_information) structure.

### -field IdSlotFlags1

The EISA slot identification flags.

### -field IdSlotFlags2

The EISA slot identification flags.

### -field MinorRevision

Information supplied by the manufacturer.

### -field MajorRevision

Information supplied by the manufacturer.

### -field Selections

The EISA selections for the device.

### -field FunctionFlags

Indicates which of the members has available information. Callers can use the following system-defined masks to determine whether a particular type of configuration information can be or has been returned by **HalGetBusData** or [HalGetBusDataByOffset](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85)):

EISA_FUNCTION_ENABLED

EISA_FREE_FORM_DATA

EISA_HAS_PORT_INIT_ENTRY

EISA_HAS_PORT_RANGE

EISA_HAS_DMA_ENTRY

EISA_HAS_IRQ_ENTRY

EISA_HAS_MEMORY_ENTRY

EISA_HAS_TYPE_ENTRY

EISA_HAS_INFORMATION

The EISA_HAS_INFORMATION mask is a combination of the following:

EISA_HAS_PORT_RANGE

EISA_HAS_DMA_ENTRY

EISA_HAS_IRQ_ENTRY

EISA_HAS_MEMORY_ENTRY

EISA_HAS_TYPE_ENTRY

### -field TypeString

Specifies the type of device.

### -field EisaMemory

Describes the EISA device memory configuration information, defined as follows:

```cpp
typedef struct _EISA_MEMORY_CONFIGURATION {
    EISA_MEMORY_TYPE ConfigurationByte;
    UCHAR DataSize;
    USHORT AddressLowWord;
    UCHAR AddressHighByte;
    USHORT MemorySize;
} EISA_MEMORY_CONFIGURATION, *PEISA_MEMORY_CONFIGURATION;
```

### -field EisaIrq

Describes the EISA interrupt configuration information, defined as follows:

```cpp
typedef struct _EISA_IRQ_CONFIGURATION {
    EISA_IRQ_DESCRIPTOR ConfigurationByte;
    UCHAR Reserved;
} EISA_IRQ_CONFIGURATION, *PEISA_IRQ_CONFIGURATION;
```

### -field EisaDma

Describes the EISA DMA configuration information, defined as follows:

```cpp
typedef struct _EISA_DMA_CONFIGURATION {
    DMA_CONFIGURATION_BYTE0 ConfigurationByte0;
    DMA_CONFIGURATION_BYTE1 ConfigurationByte1;
} EISA_DMA_CONFIGURATION, *PEISA_DMA_CONFIGURATION;
```

### -field EisaPort

Describes the EISA device port configuration information, defined as follows:

```cpp
typedef struct _EISA_PORT_CONFIGURATION {
    EISA_PORT_DESCRIPTOR Configuration;
    USHORT PortAddress;
} EISA_PORT_CONFIGURATION, *PEISA_PORT_CONFIGURATION;
```

### -field InitializationData

Vendor-supplied, device-specific initialization data, if any.

## -remarks

The information returned by **HalGetBusData** or **HalGetBusDataByOffset** in **CM_EISA_FUNCTION_INFORMATION** and/or in the [CM_EISA_SLOT_INFORMATION](/windows-hardware/drivers/ddi/wdm/ns-wdm-_cm_eisa_slot_information) header immediately preceding it is read-only.

## -see-also

[**CM_EISA_SLOT_INFORMATION**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_cm_eisa_slot_information)

[HalGetBusData](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))

[HalGetBusDataByOffset](/previous-versions/windows/hardware/drivers/ff546644(v=vs.85))
