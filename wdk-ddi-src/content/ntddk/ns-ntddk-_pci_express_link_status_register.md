---
UID: NS:ntddk._PCI_EXPRESS_LINK_STATUS_REGISTER
title: _PCI_EXPRESS_LINK_STATUS_REGISTER (ntddk.h)
description: The _PCI_EXPRESS_LINK_STATUS_REGISTER structure (ntddk.h) describes a PCI Express (PCIe) link status register of a PCIe capability structure.
old-location: pci\pci_express_link_status_register.htm
tech.root: PCI
ms.date: 02/24/2018
keywords: ["PCI_EXPRESS_LINK_STATUS_REGISTER structure"]
ms.keywords: "*PPCI_EXPRESS_LINK_STATUS_REGISTER, PCI.pci_express_link_status_register, PCI_EXPRESS_LINK_STATUS_REGISTER, PCI_EXPRESS_LINK_STATUS_REGISTER union [Buses], PPCI_EXPRESS_LINK_STATUS_REGISTER, PPCI_EXPRESS_LINK_STATUS_REGISTER union pointer [Buses], _PCI_EXPRESS_LINK_STATUS_REGISTER, ntddk/PCI_EXPRESS_LINK_STATUS_REGISTER, ntddk/PPCI_EXPRESS_LINK_STATUS_REGISTER, pci_struct_41d11df3-521f-4709-a30e-be70ad36db8f.xml"
req.header: ntddk.h
req.include-header: Ntddk.h, Miniport.h
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
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: PCI_EXPRESS_LINK_STATUS_REGISTER, *PPCI_EXPRESS_LINK_STATUS_REGISTER
f1_keywords:
 - _PCI_EXPRESS_LINK_STATUS_REGISTER
 - ntddk/_PCI_EXPRESS_LINK_STATUS_REGISTER
 - PPCI_EXPRESS_LINK_STATUS_REGISTER
 - ntddk/PPCI_EXPRESS_LINK_STATUS_REGISTER
 - PCI_EXPRESS_LINK_STATUS_REGISTER
 - ntddk/PCI_EXPRESS_LINK_STATUS_REGISTER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddk.h
api_name:
 - _PCI_EXPRESS_LINK_STATUS_REGISTER
 - PPCI_EXPRESS_LINK_STATUS_REGISTER
 - PCI_EXPRESS_LINK_STATUS_REGISTER
---

# _PCI_EXPRESS_LINK_STATUS_REGISTER structure (ntddk.h)


## -description

The **PCI_EXPRESS_LINK_STATUS_REGISTER** structure describes a PCI Express (PCIe) link status register of a PCIe capability structure.

## -syntax

```cpp
typedef union _PCI_EXPRESS_LINK_STATUS_REGISTER {

    struct {

        USHORT LinkSpeed:4;
        USHORT LinkWidth:6;
        USHORT Undefined:1;
        USHORT LinkTraining:1;
        USHORT SlotClockConfig:1;
        USHORT DataLinkLayerActive:1;
        USHORT Rsvd:2;
    } DUMMYSTRUCTNAME;

    USHORT AsUSHORT;

} PCI_EXPRESS_LINK_STATUS_REGISTER, *PPCI_EXPRESS_LINK_STATUS_REGISTER;
```

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field AsUSHORT

A **USHORT** representation of the contents of the **PCI_EXPRESS_LINK_STATUS_REGISTER** structure.


### -field DUMMYSTRUCTNAME.DataLinkLayerActive

A single bit that indicates that the data link control and management state machine is in the data link active state.


### -field DUMMYSTRUCTNAME.LinkSpeed

The negotiated link speed of the PCIe link. The encoded value specifies a Bit Location in the SupportedLinkSpeedsVector (Link Capabilities 2 Register) that corresponds to the negotiated link speed. Supported values are:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>1</b></td>
<td>2.5 GT/s (SupportedLinkSpeedsVector field bit 0)</td>
</tr>
<tr>
<td><b>2</b></td>
<td>5.0 GT/s (SupportedLinkSpeedsVector field bit 1)</td>
</tr>
<tr>
<td><b>3</b></td>
<td>8.0 GT/s (SupportedLinkSpeedsVector field bit 2)</td>
</tr>
<tr>
<td><b>4</b></td>
<td>16.0 GT/s (SupportedLinkSpeedsVector field bit 3)</td>
</tr>
<tr>
<td><b>5</b></td>
<td>32.0 GT/s (SupportedLinkSpeedsVector field bit 4)</td>
</tr>
<tr>
<td>All other values</td>
<td>Reserved.</td>
</tr>
</table>
 


### -field DUMMYSTRUCTNAME.LinkTraining

A single bit that indicates that the link is in the configuration or recovery state, or that a 1 was written to the retrain link bit of the PCIe link control register and the training has not yet begun. This member is not applicable to endpoint devices and upstream ports of switches.


### -field DUMMYSTRUCTNAME.LinkWidth

The negotiated link width (number of lanes) of the PCIe link. Possible values are:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>1</b></td>
<td>x1 (1 lane)</td>
</tr>
<tr>
<td><b>2</b></td>
<td>x2 (2 lanes)</td>
</tr>
<tr>
<td><b>4</b></td>
<td>x4 (4 lanes)</td>
</tr>
<tr>
<td><b>8</b></td>
<td>x8 (8 lanes)</td>
</tr>
<tr>
<td><b>12</b></td>
<td>x12 (12 lanes)</td>
</tr>
<tr>
<td><b>16</b></td>
<td>x16 (16 lanes)</td>
</tr>
<tr>
<td><b>32</b></td>
<td>x32 (32 lanes)</td>
</tr>
<tr>
<td>All other values</td>
<td>Reserved.</td>
</tr>
</table>
 


### -field DUMMYSTRUCTNAME.Rsvd

Reserved.


### -field DUMMYSTRUCTNAME.SlotClockConfig

A single bit that indicates that the component uses the same physical reference clock that the hardware platform provides on the PCIe slot connector. If this bit is clear, the component uses an independent clock irrespective of the presence of a reference clock on the PCIe slot connector.


### -field DUMMYSTRUCTNAME.Undefined

Reserved. Device drivers and other system software should ignore any value read from this bit.

## -syntax

```cpp
typedef union _PCI_EXPRESS_LINK_STATUS_REGISTER {
  struct {
    USHORT LinkSpeed  :4;
    USHORT LinkWidth  :6;
    USHORT Undefined  :1;
    USHORT LinkTraining  :1;
    USHORT SlotClockConfig  :1;
    USHORT DataLinkLayerActive  :1;
    USHORT Rsvd  :2;
  };
  USHORT AsUSHORT;
} PCI_EXPRESS_LINK_STATUS_REGISTER, *PPCI_EXPRESS_LINK_STATUS_REGISTER;
```

## -remarks

The **PCI_EXPRESS_LINK_STATUS_REGISTER** structure is available in Windows Server 2008 and later versions of Windows.

A **PCI_EXPRESS_LINK_STATUS_REGISTER** structure is contained in the [PCI_EXPRESS_CAPABILITY_REGISTER](ns-ntddk-_pci_express_capability.md) structure.

## -see-also

[PCI_EXPRESS_CAPABILITY_REGISTER](ns-ntddk-_pci_express_capability.md)

[PCI_EXPRESS_LINK_STATUS_2_REGISTER](ns-ntddk-pci_express_link_status_2_register.md)

