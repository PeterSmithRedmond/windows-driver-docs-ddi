---
UID: NS:nbllso._NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
title: NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
ms.date: 11/30/2020
targetos: Windows
description: The NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO structure specifies information that is used in offloading large send offload (LSO) tasks from the TCP/IP transport to a miniport adapter.
tech.root: netvista
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ndis/nbllso.h
req.include-header: ndis.h
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO, *PNDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nbllso.h
api_name:
 - _NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
 - PNDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
 - NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
f1_keywords:
 - _NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
 - nbllso/_NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
 - PNDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
 - nbllso/PNDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
 - NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
 - nbllso/NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO
dev_langs:
 - c++
---

# _NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO structure


## -description

The <b>NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO</b> structure specifies information that is used in
  offloading large send offload (LSO) tasks from the TCP/IP transport to a miniport adapter. The
  <b>NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO</b> structure is part of the 
  <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer_list">NET_BUFFER_LIST</a> information.

## -struct-fields

### -field Transmit

A structure within NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO that specifies transmit
      information and that contains the following members:

### -field Transmit.Unused

A ULONG value that specifies unused space that is reserved for NDIS.

### -field Transmit.Type

The offload type that the miniport driver should run. Protocol drivers set this member to
        NDIS_TCP_LARGE_SEND_OFFLOAD_V1_TYPE to specify large send offload version 1 (LSOV1) operations or to
        NDIS_TCP_LARGE_SEND_OFFLOAD_V2_TYPE to specify large send offload version 2 (LSOV2)
        operations.

### -field Transmit.Reserved2

Reserved for NDIS.

### -field LsoV1Transmit

A structure within NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO that specifies LSO transmit
      information and that contains the following members:

### -field LsoV1Transmit.MSS

The maximum segment size (MSS), in bytes, for each packet after segmentation. The TCP/IP
        transport writes this value before passing a large TCP packet to a miniport driver for segmentation.
        The size of TCP payload in each transmitted segment must not exceed this value.

### -field LsoV1Transmit.TcpHeaderOffset

The offset, in bytes, of the TCP header from the beginning of the packet for TCP packets.
        Miniport drivers can use 
        <b>TcpHeaderOffset</b> to determine the location of the TCP header so that they do not have to parse
        IP headers.

### -field LsoV1Transmit.Type

The offload type that the miniport driver should run. Protocol drivers set this member to
        NDIS_TCP_LARGE_SEND_OFFLOAD_V1_TYPE to specify LSOV1 operations or to
        NDIS_TCP_LARGE_SEND_OFFLOAD_V2_TYPE to specify LSOV2 operations.

### -field LsoV1Transmit.Reserved2

Reserved for NDIS.

### -field LsoV1TransmitComplete

A structure within NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO that specifies LSO transmit
      complete information and that contains the following members:

### -field LsoV1TransmitComplete.TcpPayload

The total number of TCP payload bytes in a set of packets that a network interface card (NIC)
        created by segmenting a large packet. A miniport driver writes the TCP payload size before completing
        the send of an LSO packet.

### -field LsoV1TransmitComplete.Type

The offload type that the miniport driver performed. The miniport drivers leaves this value the
        same as it was when the overlying driver submitted the packet for transmit.

### -field LsoV1TransmitComplete.Reserved2

Reserved for NDIS.

### -field LsoV2Transmit

A structure within NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO that specifies LSOV2 transmit
      information and that contains the following members:

### -field LsoV2Transmit.MSS

The MSS, in bytes, for each TCP segment. The TCP/IP transport writes this value before passing
        a large TCP packet to a miniport driver for segmentation.

### -field LsoV2Transmit.TcpHeaderOffset

The offset, in bytes, of the TCP header from the beginning of the packet for TCP packets.
        Miniport drivers can use 
        <b>TcpHeaderOffset</b> to determine the location of the TCP header so that they do not have to parse
        IP headers.

### -field LsoV2Transmit.Type

The offload type that the miniport driver should run. Protocol drivers set this member to
        NDIS_TCP_LARGE_SEND_OFFLOAD_V1_TYPE to specify LSOV1 operations or to
        NDIS_TCP_LARGE_SEND_OFFLOAD_V2_TYPE to specify LSOV2 operations.

### -field LsoV2Transmit.IPVersion

The IP version of the packet. For IPv4 packets, 
        <b>IPVersion</b> is set to NDIS_TCP_LARGE_SEND_OFFLOAD_IPv4. For IPv6 packets, 
        <b>IPVersion</b> is set to NDIS_TCP_LARGE_SEND_OFFLOAD_IPv6.

### -field LsoV2TransmitComplete

A structure within NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO that specifies LSOV2 transmit
      complete information and that contains the following members:

### -field LsoV2TransmitComplete.Reserved

In general, this member is reserved for NDIS.  However, when a send operation is complete, the miniport driver must set this member to zero.

### -field LsoV2TransmitComplete.Type

The offload type that the miniport driver performed. The miniport driver leaves this value the
        same as it was when the overlying driver submitted the packet for transmit.

 For example, when a send operation is complete, the miniport driver sets this member to <b>NDIS_TCP_LARGE_SEND_OFFLOAD_V2_TYPE</b>.

### -field LsoV2TransmitComplete.Reserved2

Reserved for NDIS.

### -field Value

A PVOID version of the LSO information. Use this member to access the raw information instead of
      the specific fields.

## -remarks

The <b>NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO</b> structure specifies information for LSOV1 and
    LSOV2 operations. The <b>NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO</b> structure is part of the
    information that is included in a 
    <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer_list">NET_BUFFER_LIST</a> structure.

To set and get the LSOV1 or LSOV2 information, use the 
    <b>TcpLargeSendNetBufferListInfo</b> index with the 
    <a href="/windows-hardware/drivers/network/net-buffer-list-info">NET_BUFFER_LIST_INFO</a> macro.
    <b>NET_BUFFER_LIST_INFO</b> returns a ULONG value (not a pointer to a ULONG value).

The TCP/IP transport updates the 
    <b>MSS</b> and 
    <b>TcpHeaderOffset</b> members of the <b>NDIS_TCP_LARGE_SEND_OFFLOAD_NET_BUFFER_LIST_INFO</b> structure before
    sending a large packet to a miniport driver.

For LSOV1, miniport drivers write the TCP payload size in the 
    <b>TcpPayload</b> member before completing a send operation for a segmented packet.

<div class="alert"><b>Note</b>  Any <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer_list">NET_BUFFER_LIST</a> structure that contains the LSOv1 or LSOv2 information also
    contains a single 
    <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer">NET_BUFFER</a> structure.</div>
<div> </div>

## -see-also

<a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer">NET_BUFFER</a>



<a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer_list">NET_BUFFER_LIST</a>



<a href="/windows-hardware/drivers/network/net-buffer-list-info">NET_BUFFER_LIST_INFO</a>



<a href="/windows-hardware/drivers/network/offloading-the-segmentation-of-large-tcp-packets">Offloading the Segmentation of Large TCP Packets</a>
