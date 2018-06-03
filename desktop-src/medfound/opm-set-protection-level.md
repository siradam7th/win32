---
Description: Sets the protection level for an output protection mechanism.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM\_SET\_PROTECTION\_LEVEL
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# OPM\_SET\_PROTECTION\_LEVEL

Sets the protection level for an output protection mechanism.



|              |                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------|
| Command GUID | OPM\_SET\_PROTECTION\_LEVEL                                                                         |
| Input data   | An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-_opm_set_protection_level_parameters) structure |



 

## Remarks

Some connectors can support multiple protection mechanisms. With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.

## Requirements



|                                     |                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                      |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## See also

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM Commands](opm-commands.md)
</dt> </dl>

 

 



