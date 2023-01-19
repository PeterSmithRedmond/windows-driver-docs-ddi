---
UID: NC:wdm.FPGA_BUS_SCAN
title: FPGA_BUS_SCAN (wdm.h)
description: Reserved for future use. Triggers a bus scan at the parent of the FPGA device.
ms.date: 01/19/2023
tech.root: kernel
keywords: ["FPGA_BUS_SCAN callback function"]
req.header: wdm.h
req.include-header: Wdm.h
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: DISPATCH_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - FPGA_BUS_SCAN
 - wdm/FPGA_BUS_SCAN
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - wdm.h
api_name:
 - FPGA_BUS_SCAN
---

## -description

Reserved for future use.

Triggers a bus scan at the parent of the FPGA device.

## -parameters

### -param Context [_In_reads_opt_(_Inexpressible_("varies"))]

The handle to the bus extension.

## -remarks

A device driver that successfully queries for the GUID_PCI_FPGA_CONTROL_INTERFACE interface receives a pointer to a [**FPGA_CONTROL_INTERFACE**](ns-wdm-_fpga_control_interface.md) structure in which the driver sets the **BusScan** member to a pointer to its implementation of the _FPGA_BUS_SCAN_ callback function.

## -see-also
