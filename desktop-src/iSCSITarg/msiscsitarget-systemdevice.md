---
title: MSISCSITARGET\_SystemDevice class
description: Associates logical devices to the MSFTSM\_System in which they are aggregated.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 736fb137-838b-4674-bfee-262ef183ca44
ms.prod: windows-server-dev
ms.technology:
- iscsi-target
- windows-management-instrumentation
ms.tgt_platform: multiple
keywords:
- MSISCSITARGET_SystemDevice class iSCSI Software Target API
- MSISCSITARGET_SystemDevice class iSCSI Software Target API , described
topic_type:
- apiref
api_name:
- MSISCSITARGET_SystemDevice
- MSISCSITARGET_SystemDevice.GroupComponent
- MSISCSITARGET_SystemDevice.PartComponent
api_location:
- SMiSCSITargetProv.dll
api_type:
- DllExport
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MSISCSITARGET\_SystemDevice class

Associates logical devices to the [**MSFTSM\_System**](msftsm-system.md) in which they are aggregated.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.

## Syntax

``` syntax
[Dynamic, Provider("MSiSCSITargetProv"), Association, Aggregation, Composition, Version("1.0.0")]
class MSISCSITARGET_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## Members

The **MSISCSITARGET\_SystemDevice** class has these types of members:

-   [Properties](#properties)

### Properties

The **MSISCSITARGET\_SystemDevice** class has these properties.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Data type: **CIM\_System**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Aggregate**](https://msdn.microsoft.com/library/aa393650), [**Min**](https://msdn.microsoft.com/library/aa393650) (1), [**Max**](https://msdn.microsoft.com/library/aa393650) (1)
</dt> </dl>

The parent system in the Association.

This property is inherited from [**CIM\_SystemDevice**](cim-systemdevice.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Data type: **CIM\_LogicalDevice**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Weak**](https://msdn.microsoft.com/library/aa393650)
</dt> </dl>

The LogicalDevice that is a component of a System.

This property is inherited from [**CIM\_SystemDevice**](cim-systemdevice.md).

</dd> </dl>

## Requirements



|                                     |                                                                                                  |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                        |
| Minimum supported server<br/> | Windows Server 2012 R2<br/>                                                                |
| Namespace<br/>                | Root\\CIMv2\\Storage\\iScsiTarget<br/>                                                     |
| MOF<br/>                      | <dl> <dt>SmIscsiTarget.mof</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>SMiSCSITargetProv.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_SystemDevice**](cim-systemdevice.md)
</dt> <dt>

[iSCSI Target Server Reference](https://msdn.microsoft.com/library/hh830439)
</dt> <dt>

[**MSFTSM\_System**](msftsm-system.md)
</dt> <dt>

[**CIM\_LogicalDevice**](https://msdn.microsoft.com/library/aa387884)
</dt> </dl>

 

 




