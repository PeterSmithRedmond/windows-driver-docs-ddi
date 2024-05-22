---
UID: NF:netadapter.NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED
title: NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED function (netadapter.h)
description: The NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED function initializes a NET_ADAPTER_RX_CAPABILITIES structure for a net adapter that would like to specify driver-managed receive buffer allocation and attachment.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED function"]
ms.keywords: NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.25
req.umdf-ver: 2.33 
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
 - NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED
 - netadapter/NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED
---

# NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED function


## -description

The **NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED** function initializes a [**NET_ADAPTER_RX_CAPABILITIES**](ns-netadapter-_net_adapter_rx_capabilities.md) structure for a net adapter that would like to specify driver-managed receive buffer allocation and attachment.

## -parameters

### -param RxCapabilities [_Out_]

A pointer to a driver-allocated [**NET_ADAPTER_RX_CAPABILITIES**](ns-netadapter-_net_adapter_rx_capabilities.md) structure.

### -param EvtAdapterReturnRxBuffer [_In_]

A pointer to the client driver's *EVT_NET_ADAPTER_RETURN_RX_BUFFER* callback function. For more information, see the Remarks section.

### -param MaximumFrameSize [_In_]

The maximum frame size, in bytes, that the adapter can receive.

### -param MaximumNumberOfQueues [_In_]

The maximum number of receive queues that the adapter supports.

## -remarks

This function is one of three possible functions to call in order to initialize a [**NET_ADAPTER_RX_CAPABILITIES**](ns-netadapter-_net_adapter_rx_capabilities.md) structure. Which one the client driver should call depends on how it would like to allocate receive buffers and if it would like to use DMA.

The client driver must call **NET_ADAPTER_RX_CAPABILITIES_INIT_DRIVER_MANAGED** to initialize its **NET_ADAPTER_RX_CAPABILITIES** structure if it would like to perform manual receive buffer allocation and attachment. By calling this function, the Rx capabilities structure's **AllocationMode** member is set to **NetRxFragmentBufferAllocationModeDriver** and the **AttachmentMode** member is set to **NetRxFragmentBufferAttachmentModeDriver**. In this case, it must also provide a pointer to its *EVT_NET_ADAPTER_RETURN_RX_BUFFER* callback function in the structure for the operating system to invoke once the system has finished with the receive buffer.

## -see-also

[**NET_ADAPTER_RX_CAPABILITIES**](ns-netadapter-_net_adapter_rx_capabilities.md)

[**NET_ADAPTER_RX_CAPABILITIES_INIT_SYSTEM_MANAGED**](nf-netadapter-net_adapter_rx_capabilities_init_system_managed.md)

[**NET_ADAPTER_RX_CAPABILITIES_INIT_SYSTEM_MANAGED_DMA**](nf-netadapter-net_adapter_rx_capabilities_init_system_managed_dma.md)

