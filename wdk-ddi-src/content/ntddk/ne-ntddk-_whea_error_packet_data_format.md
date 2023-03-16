---
UID: NE:ntddk._WHEA_ERROR_PACKET_DATA_FORMAT
title: _WHEA_ERROR_PACKET_DATA_FORMAT (ntddk.h)
description: The WHEA_ERROR_PACKET_DATA_FORMAT enumeration defines the raw hardware error data format in a hardware error packet.
tech.root: whea
ms.date: 03/13/2023
keywords: ["WHEA_ERROR_PACKET_DATA_FORMAT enumeration"]
ms.keywords: "*PWHEA_ERROR_PACKET_DATA_FORMAT, PWHEA_ERROR_PACKET_DATA_FORMAT, PWHEA_ERROR_PACKET_DATA_FORMAT enumeration pointer [WHEA Drivers and Applications], WHEA_ERROR_PACKET_DATA_FORMAT, WHEA_ERROR_PACKET_DATA_FORMAT enumeration [WHEA Drivers and Applications], WheaDataFormatGeneric, WheaDataFormatIPFSalRecord, WheaDataFormatMax, WheaDataFormatMemory, WheaDataFormatNMIPort, WheaDataFormatPCIExpress, WheaDataFormatPCIXBus, WheaDataFormatPCIXDevice, WheaDataFormatXPFMCA, _WHEA_ERROR_PACKET_DATA_FORMAT, ntddk/PWHEA_ERROR_PACKET_DATA_FORMAT, ntddk/WHEA_ERROR_PACKET_DATA_FORMAT, ntddk/WheaDataFormatGeneric, ntddk/WheaDataFormatIPFSalRecord, ntddk/WheaDataFormatMax, ntddk/WheaDataFormatMemory, ntddk/WheaDataFormatNMIPort, ntddk/WheaDataFormatPCIExpress, ntddk/WheaDataFormatPCIXBus, ntddk/WheaDataFormatPCIXDevice, ntddk/WheaDataFormatXPFMCA, whea.whea_error_packet_data_format, whearef_19f75c8f-94d0-4837-ab44-e9ba9fbe51f7.xml"
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: Supported in Windows 7 and later versions of Windows.
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
req.typenames: WHEA_ERROR_PACKET_DATA_FORMAT, *PWHEA_ERROR_PACKET_DATA_FORMAT
f1_keywords:
 - _WHEA_ERROR_PACKET_DATA_FORMAT
 - ntddk/_WHEA_ERROR_PACKET_DATA_FORMAT
 - PWHEA_ERROR_PACKET_DATA_FORMAT
 - ntddk/PWHEA_ERROR_PACKET_DATA_FORMAT
 - WHEA_ERROR_PACKET_DATA_FORMAT
 - ntddk/WHEA_ERROR_PACKET_DATA_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddk.h
api_name:
 - _WHEA_ERROR_PACKET_DATA_FORMAT
 - PWHEA_ERROR_PACKET_DATA_FORMAT
 - WHEA_ERROR_PACKET_DATA_FORMAT
---

## -description

The WHEA_ERROR_PACKET_DATA_FORMAT enumeration defines the raw hardware error data format in a hardware error packet.

## -enum-fields

### -field WheaDataFormatIPFSalRecord

The raw data in the hardware error packet contains an Itanium processor family system abstraction layer (SAL) error record. For more information about the format of a SAL error record, see the [Intel Itanium Processor Family System Abstraction Layer Specification](https://www.intel.com/content/dam/www/public/us/en/documents/specification-updates/itanium-system-abstraction-layer-specification.pdf).

### -field WheaDataFormatXPFMCA

The raw data in the hardware error packet is formatted as an MCA_EXCEPTION structure. For more information about the MCA_EXCEPTION structure, see [HalQuerySystemInformation](/previous-versions/windows/hardware/mca/ff540659(v=vs.85)).

### -field WheaDataFormatMemory

The raw data in the hardware error packet contains memory error data. The format of this error data is dependent on the memory architecture.

### -field WheaDataFormatPCIExpress

The raw data in the hardware error packet is formatted as a [PCI_EXPRESS_AER_CAPABILITY](../wdm/ns-wdm-_pci_express_aer_capability.md) structure.

### -field WheaDataFormatNMIPort

The raw data in the hardware error packet contains the data that was read from the nonmaskable interrupt (NMI) I/O ports by the NMI low-level hardware error handler (LLHEH). The format of this error data is specific to the implementation.

### -field WheaDataFormatPCIXBus

The raw data in the hardware error packet contains PCI/PCI-X bus error data. The format of this error data is specific to the implementation.

### -field WheaDataFormatPCIXDevice

The raw data in the hardware error packet contains a PCI/PCI-X device error data. The format of this error data is specific to the implementation.

### -field WheaDataFormatGeneric

The raw data in the hardware error packet is formatted as a [WHEA_GENERIC_ERROR](./ns-ntddk-_whea_generic_error.md) structure.

### -field WheaDataFormatMax

The maximum number of formats of raw hardware error data.

## -remarks

The [WHEA_ERROR_PACKET_V2](./ns-ntddk-_whea_error_packet_v2.md) structure contains a member of type WHEA_ERROR_PACKET_DATA_FORMAT that specifies the format of the raw data that is contained in the hardware error packet.

## -see-also

[PCI_EXPRESS_AER_CAPABILITY](../wdm/ns-wdm-_pci_express_aer_capability.md)

[WHEA_ERROR_PACKET_V2](./ns-ntddk-_whea_error_packet_v2.md)

[WHEA_GENERIC_ERROR](./ns-ntddk-_whea_generic_error.md)