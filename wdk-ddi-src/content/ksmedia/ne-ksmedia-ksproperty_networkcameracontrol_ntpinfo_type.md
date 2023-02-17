---
UID: NE:ksmedia.KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE
title: KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE  (ksmedia.h)
description: The KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE enumeration defines the network camera control NTP types.
tech.root: stream
ms.date: 06/24/2021
ms.keywords: KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.construct-type: structure
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE
targetos: Windows
f1_keywords:
 - KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE
 - ksmedia/KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE
---

# KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE enumeration


## -description

The **KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE** enumeration defines the network camera control NTP types.

## -enum-fields

### -field KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE_DISABLE

Sets the camera into manual mode. The user can set the time on the camera manually.

### -field KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE_HOSTNTP

Sets the camera to use the same NTP server as is configured on the host.

### -field KSPROPERYT_NETWORKCAMERACONTROL_NTPINFO_TYPE_CUSTOM

Sets a specific custom NTP server on the camera.

## -remarks

If NTP is enabled on the camera, a get operation will return the name of the NTP server that is set on the Onvif protocol device.

If use of a NTP server is disabled on the camera, a get operation will return KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE_DISABLE.

## -see-also

[KSPROPERTY_NETWORKCAMERACONTROL_EVENTTOPICS_XML](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-eventtopics-xml)

[KSPROPERTY_NETWORKCAMERACONTROL_METADATA](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-metadata)

[KSPROPERTYSETID_NetworkCameraControl](/windows-hardware/drivers/stream/kspropertysetid-networkcameracontrol)

[KSPROPERTY_NETWORKCAMERACONTROL_NTP](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-ntp)

[KSPROPERTY_NETWORKCAMERACONTROL_URI](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-uri)

[KSPROPERTY_NETWORKCAMERACONTROL_EVENT_INFO](ns-ksmedia-ksproperty_networkcameracontrol_event_info.md)

[KSPROPERTY_NETWORKCAMERACONTROL_METADATA_INFO](ns-ksmedia-ksproperty_networkcameracontrol_metadata_info.md)

[KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER](ns-ksmedia-ksproperty_networkcameracontrol_ntpinfo_header.md)

[KSPROPERTY_NETWORKCAMERACONTROL_PROPERTY](ne-ksmedia-ksproperty_networkcameracontrol_property.md)

