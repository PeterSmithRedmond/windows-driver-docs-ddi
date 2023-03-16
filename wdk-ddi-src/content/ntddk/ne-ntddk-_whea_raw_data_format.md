---
UID: NE:ntddk._WHEA_RAW_DATA_FORMAT
title: _WHEA_RAW_DATA_FORMAT (ntddk.h)
description: The WHEA_RAW_DATA_FORMAT enumeration defines the possible formats that raw hardware error data can be encoded in a hardware error packet.
tech.root: whea
ms.date: 03/13/2023
keywords: ["WHEA_RAW_DATA_FORMAT enumeration"]
ms.keywords: "*PWHEA_RAW_DATA_FORMAT, PWHEA_RAW_DATA_FORMAT, PWHEA_RAW_DATA_FORMAT enumeration pointer [WHEA Drivers and Applications], WHEA_RAW_DATA_FORMAT, WHEA_RAW_DATA_FORMAT enumeration [WHEA Drivers and Applications], WheaRawDataFormatAMD64MCA, WheaRawDataFormatGeneric, WheaRawDataFormatIA32MCA, WheaRawDataFormatIPFSalRecord, WheaRawDataFormatIntel64MCA, WheaRawDataFormatMax, WheaRawDataFormatMemory, WheaRawDataFormatNMIPort, WheaRawDataFormatPCIExpress, WheaRawDataFormatPCIXBus, WheaRawDataFormatPCIXDevice, _WHEA_RAW_DATA_FORMAT, ntddk/PWHEA_RAW_DATA_FORMAT, ntddk/WHEA_RAW_DATA_FORMAT, ntddk/WheaRawDataFormatAMD64MCA, ntddk/WheaRawDataFormatGeneric, ntddk/WheaRawDataFormatIA32MCA, ntddk/WheaRawDataFormatIPFSalRecord, ntddk/WheaRawDataFormatIntel64MCA, ntddk/WheaRawDataFormatMax, ntddk/WheaRawDataFormatMemory, ntddk/WheaRawDataFormatNMIPort, ntddk/WheaRawDataFormatPCIExpress, ntddk/WheaRawDataFormatPCIXBus, ntddk/WheaRawDataFormatPCIXDevice, whea.whea_raw_data_format, whearef_9ecb0580-4372-40f3-93da-4f866ee6211f.xml"
req.header: ntddk.h
req.include-header: Ntddk.h
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
req.typenames: WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
f1_keywords:
 - _WHEA_RAW_DATA_FORMAT
 - ntddk/_WHEA_RAW_DATA_FORMAT
 - PWHEA_RAW_DATA_FORMAT
 - ntddk/PWHEA_RAW_DATA_FORMAT
 - WHEA_RAW_DATA_FORMAT
 - ntddk/WHEA_RAW_DATA_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddk.h
api_name:
 - _WHEA_RAW_DATA_FORMAT
 - PWHEA_RAW_DATA_FORMAT
 - WHEA_RAW_DATA_FORMAT
---

## -description

The WHEA_RAW_DATA_FORMAT enumeration defines the possible formats that raw hardware error data can be encoded in a hardware error packet.

## -enum-fields

### -field WheaRawDataFormatIPFSalRecord

The raw data in the hardware error packet contains an Itanium processor family system abstraction layer (SAL) error record. For more information about the format of a SAL error record, see the [Intel Itanium Processor Family System Abstraction Layer Specification](https://www.intel.com/content/dam/www/public/us/en/documents/specification-updates/itanium-system-abstraction-layer-specification.pdf).

### -field WheaRawDataFormatIA32MCA

The raw data in the hardware error packet contains an MCA_EXCEPTION structure. For more information about the MCA_EXCEPTION structure, see [HalQuerySystemInformation](/previous-versions/windows/hardware/mca/ff540659(v=vs.85)).

### -field WheaRawDataFormatIntel64MCA

The raw data in the hardware error packet contains an MCA_EXCEPTION structure. For more information about the MCA_EXCEPTION structure, see [HalQuerySystemInformation](/previous-versions/windows/hardware/mca/ff540659(v=vs.85)).

### -field WheaRawDataFormatAMD64MCA

The raw data in the hardware error packet contains an MCA_EXCEPTION structure. For more information about the MCA_EXCEPTION structure, see [HalQuerySystemInformation](/previous-versions/windows/hardware/mca/ff540659(v=vs.85)).

### -field WheaRawDataFormatMemory

The raw data in the hardware error packet contains memory error data. The format of this error data is memory architecture-dependent.

### -field WheaRawDataFormatPCIExpress

The raw data in the hardware error packet contains a [PCI_EXPRESS_AER_CAPABILITY](../wdm/ns-wdm-_pci_express_aer_capability.md) structure.

### -field WheaRawDataFormatNMIPort

The raw data in the hardware error packet contains the data that was read from the nonmaskable interrupt (NMI) I/O ports by the NMI low-level hardware error handler (LLHEH).

### -field WheaRawDataFormatPCIXBus

The raw data in the hardware error packet contains PCI/PCI-X bus error data. The format of this error data is specific to the implementation.

### -field WheaRawDataFormatPCIXDevice

The raw data in the hardware error packet contains a PCI/PCI-X device error data. The format of this error data is specific to the implementation.

### -field WheaRawDataFormatGeneric

The raw data in the hardware error packet contains a [WHEA_GENERIC_ERROR](./ns-ntddk-_whea_generic_error.md) structure.

### -field WheaRawDataFormatMax

The maximum number of formats of raw hardware error data.

## -remarks

The [WHEA_ERROR_PACKET_V1](./ns-ntddk-_whea_error_packet_v1.md) structure contains a member of type WHEA_RAW_DATA_FORMAT that specifies the format of the raw data that is contained in the hardware error packet.

## -see-also

[HalQuerySystemInformation](/previous-versions/windows/hardware/mca/ff540659(v=vs.85))

[PCI_EXPRESS_AER_CAPABILITY](../wdm/ns-wdm-_pci_express_aer_capability.md)

[WHEA_ERROR_PACKET_V1](./ns-ntddk-_whea_error_packet_v1.md)

[WHEA_GENERIC_ERROR](./ns-ntddk-_whea_generic_error.md)