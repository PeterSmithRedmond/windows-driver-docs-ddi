---
UID: NS:wdm._PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
title: _PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS (wdm.h)
description: The _PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS structure (wdm.h) describes a PCI Express (PCIe) uncorrectable error status register.
old-location: pci\pci_express_uncorrectable_error_status.htm
tech.root: PCI
ms.date: 02/24/2018
keywords: ["PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS structure"]
ms.keywords: "*PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS, PCI.pci_express_uncorrectable_error_status, PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS, PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS union [Buses], PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS, PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS union pointer [Buses], _PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS, pci_struct_9341a010-06c8-46ee-931f-2a67756c12d2.xml, wdm/PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS, wdm/PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS"
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h, Miniport.h
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
req.irql: PASSIVE_LEVEL (see Remarks section)
targetos: Windows
req.typenames: PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS, *PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
f1_keywords:
 - _PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
 - wdm/_PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
 - PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
 - wdm/PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
 - PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
 - wdm/PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - _PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
 - PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
 - PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS
---

# _PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS structure (wdm.h)


## -description

The PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS structure describes a PCI Express (PCIe) uncorrectable error status register of a PCIe advanced error reporting capability structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS structure.


### -field DUMMYSTRUCTNAME.CompleterAbort

A single bit that indicates that a completer abort has occurred.


### -field DUMMYSTRUCTNAME.CompletionTimeout

A single bit that indicates that a completion timeout has occurred.


### -field DUMMYSTRUCTNAME.DataLinkProtocolError

A single bit that indicates that a data link protocol error has occurred.


### -field DUMMYSTRUCTNAME.ECRCError

A single bit that indicates that an end-to-end cyclic redundancy check (ECRC) error has occurred.


### -field DUMMYSTRUCTNAME.FlowControlProtocolError

A single bit that indicates that a flow control protocol error has occurred.


### -field DUMMYSTRUCTNAME.MalformedTLP

A single bit that indicates that a malformed transaction layer packet (TLP) has been detected.


### -field DUMMYSTRUCTNAME.PoisonedTLP

A single bit that indicates that a poisoned transaction layer packet (TLP) has been detected.


### -field DUMMYSTRUCTNAME.ReceiverOverflow

A single bit that indicates that the receiver has overflowed.


### -field DUMMYSTRUCTNAME.Reserved1

Reserved.


### -field DUMMYSTRUCTNAME.Reserved2

Reserved.


### -field DUMMYSTRUCTNAME.Reserved3

Reserved.


### -field DUMMYSTRUCTNAME.SurpriseDownError

A single bit that indicates that a surprise down error has occurred.


### -field DUMMYSTRUCTNAME.Undefined

A single bit that contains an undefined value. In versions of the <i>PCIe Specification</i> prior to version 1.1, this bit indicates that a link training error has occurred.


### -field DUMMYSTRUCTNAME.UnexpectedCompletion

A single bit that indicates that an unexpected completion has occurred.


### -field DUMMYSTRUCTNAME.UnsupportedRequestError

A single bit that indicates that an unsupported request error has occurred.

### -field DUMMYSTRUCTNAME.AcsViolation

### -field DUMMYSTRUCTNAME.UncorrectableInternalError

### -field DUMMYSTRUCTNAME.MCBlockedTlp

### -field DUMMYSTRUCTNAME.AtomicOpEgressBlocked

### -field DUMMYSTRUCTNAME.TlpPrefixBlocked

## -syntax

```cpp
typedef union _PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS {
  struct {
    ULONG Undefined  :1;
    ULONG Reserved1  :3;
    ULONG DataLinkProtocolError  :1;
    ULONG SurpriseDownError  :1;
    ULONG Reserved2  :6;
    ULONG PoisonedTLP  :1;
    ULONG FlowControlProtocolError  :1;
    ULONG CompletionTimeout  :1;
    ULONG CompleterAbort  :1;
    ULONG UnexpectedCompletion  :1;
    ULONG ReceiverOverflow  :1;
    ULONG MalformedTLP  :1;
    ULONG ECRCError  :1;
    ULONG UnsupportedRequestError  :1;
    ULONG Reserved3  :11;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS, *PPCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS;
```

## -remarks

The PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_UNCORRECTABLE_ERROR_STATUS structure is contained in the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_aer_capability">PCI_EXPRESS_AER_CAPABILITY</a>, <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_bridge_aer_capability">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>, and <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_rootport_aer_capability">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a> structures.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_aer_capability">PCI_EXPRESS_AER_CAPABILITY</a>



<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_bridge_aer_capability">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>



<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_rootport_aer_capability">PCI_EXPRESS_ROOTPORT_AER_CAPABILITY</a>

