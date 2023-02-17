---
UID: NS:ksmedia.KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
title: KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER (ksmedia.h)
description: The KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER structure contains a NTP-specific payload that is used to set or disable an NTP server on a Onvif protocol camera.
tech.root: stream
ms.date: 06/24/2021
ms.keywords: KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER, *PKSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.construct-type: structure
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER, *PKSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
targetos: Windows
f1_keywords:
 - PKSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
 - ksmedia/PKSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
 - KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
 - ksmedia/KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ksmedia.h
api_name:
 - PKSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
 - KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER
---

# KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER structure


## -description

The **KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_HEADER** structure contains a NTP-specific payload that is used to set or disable an NTP server on a Onvif protocol camera.

## -struct-fields

### -field Size

The size of the NTP-specific payload.

### -field Type

Contains one of the values from the [KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE](/windows-hardware/drivers/ddi/content/ksmedia/ne-ksmedia-ksproperty_networkcameracontrol_ntpinfo_type) enumeration.

## -remarks

This command will be used to set or disable an NTP server on the Onvif protocol camera. The app can choose to configure the camera to use the same NTP server as is used by the local machine (for example, the Windows device that is controlling the camera.) It can also be used to configure the camera to use a custom NTP server.

The local PC's NTP server entry is found by parsing the registry value at SYSTEM\\CurrentControlSet\\Services\\W32Time\\Parameters\\. Apps can scan the space-separated registry value for the most optimal server to set on the camera.

## -see-also

[KSPROPERTY_NETWORKCAMERACONTROL_EVENTTOPICS_XML](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-eventtopics-xml)

[KSPROPERTY_NETWORKCAMERACONTROL_METADATA](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-metadata)

[KSPROPERTYSETID_NetworkCameraControl](/windows-hardware/drivers/stream/kspropertysetid-networkcameracontrol)

[KSPROPERTY_NETWORKCAMERACONTROL_NTP](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-ntp)

[KSPROPERTY_NETWORKCAMERACONTROL_URI](/windows-hardware/drivers/stream/ksproperty-networkcameracontrol-uri)

[KSPROPERTY_NETWORKCAMERACONTROL_EVENT_INFO](ns-ksmedia-ksproperty_networkcameracontrol_event_info.md)

[KSPROPERTY_NETWORKCAMERACONTROL_METADATA_INFO](ns-ksmedia-ksproperty_networkcameracontrol_metadata_info.md)

[KSPROPERTY_NETWORKCAMERACONTROL_NTPINFO_TYPE](ne-ksmedia-ksproperty_networkcameracontrol_ntpinfo_type.md)

[KSPROPERTY_NETWORKCAMERACONTROL_PROPERTY](ne-ksmedia-ksproperty_networkcameracontrol_property.md)

