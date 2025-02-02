---
UID: NS:windot11._DOT11_WFD_INVITATION_FLAGS
title: _DOT11_WFD_INVITATION_FLAGS (windot11.h)
description: The DOT11_WFD_INVITATION_FLAGS structure represents the Invitation Attributes used during the Invitation procedure.
old-location: netvista\dot11_wfd_invitation_flags.htm
tech.root: netvista
ms.date: 02/16/2018
keywords: ["DOT11_WFD_INVITATION_FLAGS structure"]
ms.keywords: "*PDOT11_WFD_INVITATION_FLAGS, DOT11_WFD_INVITATION_FLAGS, DOT11_WFD_INVITATION_FLAGS structure [Network Drivers Starting with Windows Vista], Join, PDOT11_WFD_INVITATION_FLAGS, PDOT11_WFD_INVITATION_FLAGS structure pointer [Network Drivers Starting with Windows Vista], Reinvoke, _DOT11_WFD_INVITATION_FLAGS, netvista.dot11_wfd_invitation_flags, windot11/DOT11_WFD_INVITATION_FLAGS, windot11/PDOT11_WFD_INVITATION_FLAGS"
req.header: windot11.h
req.include-header: Windot11.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with   Windows 8.
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
req.typenames: DOT11_WFD_INVITATION_FLAGS, *PDOT11_WFD_INVITATION_FLAGS
f1_keywords:
 - _DOT11_WFD_INVITATION_FLAGS
 - windot11/_DOT11_WFD_INVITATION_FLAGS
 - PDOT11_WFD_INVITATION_FLAGS
 - windot11/PDOT11_WFD_INVITATION_FLAGS
 - DOT11_WFD_INVITATION_FLAGS
 - windot11/DOT11_WFD_INVITATION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windot11.h
api_name:
 - _DOT11_WFD_INVITATION_FLAGS
 - PDOT11_WFD_INVITATION_FLAGS
 - DOT11_WFD_INVITATION_FLAGS
---

# _DOT11_WFD_INVITATION_FLAGS structure


## -description

<div class="alert"><b>Important</b>  The <a href="/previous-versions/windows/hardware/wireless/ff560689(v=vs.85)">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="/windows-hardware/drivers/network/wifi-universal-driver-model">WLAN Universal Windows driver model</a>.</div><div> </div>The <b>DOT11_WFD_INVITATION_FLAGS</b> structure represents the Invitation Attributes used during the Invitation procedure.

## -struct-fields

### -field InvitationType

The type of group invitation. The invitation types have the following meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Join"></a><a id="join"></a><a id="JOIN"></a><dl>
<dt><b>Join</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
An invitation to join an active group.

</td>
</tr>
<tr>
<td width="40%"><a id="Reinvoke"></a><a id="reinvoke"></a><a id="REINVOKE"></a><dl>
<dt><b>Reinvoke</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The invitation is reinvoked.

</td>
</tr>
</table>
 


### -field Reserved

Reserved.

## -syntax

```cpp
typedef struct _DOT11_WFD_INVITATION_FLAGS {
  UCHAR InvitationType:1;
  UCHAR Reserved:7;
} DOT11_WFD_INVITATION_FLAGS, *PDOT11_WFD_INVITATION_FLAGS;
```

