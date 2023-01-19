---
UID: NC:wdm.IOMMU_DEVICE_FAULT_HANDLER
title: IOMMU_DEVICE_FAULT_HANDLER (wdm.h)
description: Reports fault from a specific device and domain.
tech.root: kernel
ms.date: 01/19/2023
keywords: ["IOMMU_DEVICE_FAULT_HANDLER callback function"]
req.header: wdm.h
req.include-header: Wdm.h
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1809
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - IOMMU_DEVICE_FAULT_HANDLER
 - wdm/IOMMU_DEVICE_FAULT_HANDLER
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - wdm.h
api_name:
 - IOMMU_DEVICE_FAULT_HANDLER
---

## -description

Reports fault from a specific device and domain.

## -parameters

### -param Context

A pointer to the opaque driver-supplied fault context.

### -param FaultInformation

A pointer to a [**FAULT_INFORMATION**](ns-wdm-_fault_information.md) structure that contains fault information.

## -remarks

Register your implementation of this callback function by setting the **FaultHandler** member of [**DEVICE_FAULT_CONFIGURATION**](ns-wdm-_device_fault_configuration.md).

## -see-also
