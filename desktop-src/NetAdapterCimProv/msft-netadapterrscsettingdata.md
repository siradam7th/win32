---
Description: RSC properties for a network adapter.
ms.assetid: c720e56f-6bf0-4744-ba71-57c50126db4f
title: MSFT\_NetAdapterRscSettingData class
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MSFT\_NetAdapterRscSettingData class

RSC properties for a network adapter.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.

## Syntax

``` syntax
[Dynamic, Provider("NetAdapterCim")]
class MSFT_NetAdapterRscSettingData : MSFT_NetAdapterSettingData
{
  string  Caption;
  string  Description;
  string  ElementName;
  string  InstanceID;
  string  Name;
  string  InterfaceDescription;
  uint32  Source;
  string  SystemName;
  boolean IPv4Enabled;
  boolean IPv6Enabled;
  string  RscHardwareCapabilities;
  boolean IPv4OperationalState;
  boolean IPv6OperationalState;
  uint32  IPv4FailureReason;
  uint32  IPv6FailureReason;
};
```

## Members

The **MSFT\_NetAdapterRscSettingData** class has these types of members:

-   [Methods](#methods)
-   [Properties](#properties)

### Methods

The **MSFT\_NetAdapterRscSettingData** class has these methods.



| Method                                                   | Description                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Disable**](disable-msft-netadapterrscsettingdata.md) | Disables the Receive Segment Coalescing (RSC) properties on the network adapter.<br/> |
| [**Enable**](enable-msft-netadapterrscsettingdata.md)   | Enables the Receive Segment Coalescing (RSC) properties on the network adapter.<br/>  |



 

### Properties

The **MSFT\_NetAdapterRscSettingData** class has these properties.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **MaxLen** ( 64 )
</dt> </dl>

A short textual description of the object. This property inherits from [**CIM\_ManagedElement**](https://msdn.microsoft.com/library/mt432218).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

A textual description of the object. This property inherits from [**CIM\_ManagedElement**](https://msdn.microsoft.com/library/mt432218).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

A user-friendly name for the object. This property enables each instance to define a display name in addition to its key properties, identity data, and description information. Be aware that the Name property of ManagedSystemElement is also defined as a display name. However, it is often subclassed to be a Key. The same property can convey both identity and a user-friendly name, without inconsistencies. Where Name exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the Name and ElementName properties. This property inherits from [**CIM\_ManagedElement**](https://msdn.microsoft.com/library/mt432218).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **Key**
</dt> </dl>

Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class. To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority. (This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:). When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*. *LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements. If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance. For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.

This property inherits from [**CIM\_SettingData**](https://msdn.microsoft.com/library/mt432316).

</dd> <dt>

**InterfaceDescription**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Interface Description, also known as "ifDesc" or display name is a unique name assigned to the network adapter during installation. This name cannot be changed and is persisted as long as the network adapter is not uninstalled. This property inherits from [**MSFT\_NetAdapterSettingData**](msft-netadaptersettingdata.md).

</dd> <dt>

**IPv4Enabled**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read/write
</dt> </dl>

Controls RSC setting for IPv4 TCP packets.

</dd> <dt>

**IPv4FailureReason**
</dt> <dd> <dl> <dt>

Data type: **uint32**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates the cause for RSC being disabled for IPv4 TCP packets.

<dl> <dt>

<span id="NoFailure"></span><span id="nofailure"></span><span id="NOFAILURE"></span>**NoFailure** (0)
</dt> <dt>

<span id="NicPropertyDisabled"></span><span id="nicpropertydisabled"></span><span id="NICPROPERTYDISABLED"></span>**NicPropertyDisabled** (1)
</dt> <dt>

<span id="WFPCompatibility"></span><span id="wfpcompatibility"></span><span id="WFPCOMPATIBILITY"></span>**WFPCompatibility** (2)
</dt> <dt>

<span id="NDISCompatibility"></span><span id="ndiscompatibility"></span><span id="NDISCOMPATIBILITY"></span>**NDISCompatibility** (3)
</dt> <dt>

<span id="ForwardingEnabled"></span><span id="forwardingenabled"></span><span id="FORWARDINGENABLED"></span>**ForwardingEnabled** (4)
</dt> <dt>

<span id="NetOffloadGlobalDisabled"></span><span id="netoffloadglobaldisabled"></span><span id="NETOFFLOADGLOBALDISABLED"></span>**NetOffloadGlobalDisabled** (5)
</dt> </dl>

</dd> <dt>

**IPv4OperationalState**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates if RSC is currently operational for IPv4 TCP packets.

</dd> <dt>

**IPv6Enabled**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read/write
</dt> </dl>

Controls RSC setting for IPv6 TCP packets.

</dd> <dt>

**IPv6FailureReason**
</dt> <dd> <dl> <dt>

Data type: **uint32**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates the cause for RSC being disabled for IPv6 TCP packets.

<dl> <dt>

<span id="NoFailure"></span><span id="nofailure"></span><span id="NOFAILURE"></span>**NoFailure** (0)
</dt> <dt>

<span id="NicPropertyDisabled"></span><span id="nicpropertydisabled"></span><span id="NICPROPERTYDISABLED"></span>**NicPropertyDisabled** (1)
</dt> <dt>

<span id="WFPCompatibility"></span><span id="wfpcompatibility"></span><span id="WFPCOMPATIBILITY"></span>**WFPCompatibility** (2)
</dt> <dt>

<span id="NDISCompatibility"></span><span id="ndiscompatibility"></span><span id="NDISCOMPATIBILITY"></span>**NDISCompatibility** (3)
</dt> <dt>

<span id="ForwardingEnabled"></span><span id="forwardingenabled"></span><span id="FORWARDINGENABLED"></span>**ForwardingEnabled** (4)
</dt> <dt>

<span id="NetOffloadGlobalDisabled"></span><span id="netoffloadglobaldisabled"></span><span id="NETOFFLOADGLOBALDISABLED"></span>**NetOffloadGlobalDisabled** (5)
</dt> </dl>

</dd> <dt>

**IPv6OperationalState**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates if RSC is currently operational for IPv6 TCP packets.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Name, also known as Connection Name, "ifAlias", or InterfaceAlias, is a unique name assigned to the adapter during installation. The Name of the adapter can be changed by the administrator and is persisted across the boot or network adapter restart. This property inherits from [**MSFT\_NetAdapterSettingData**](msft-netadaptersettingdata.md).

</dd> <dt>

**RscHardwareCapabilities**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

The RSC hardware capabilities of the Adapter.

</dd> <dt>

**Source**
</dt> <dd> <dl> <dt>

Data type: **uint32**
</dt> <dt>

Access type: Read-only
</dt> </dl>

The source of the setting data. This property inherits from [**MSFT\_NetAdapterSettingData**](msft-netadaptersettingdata.md).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)
</dt> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>**Device** (2)
</dt> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>**Persistent storage** (3)
</dt> </dl>

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

The scoping System\\'s Name. This property inherits from [**MSFT\_NetAdapterSettingData**](msft-netadaptersettingdata.md).

</dd> </dl>

## Requirements



|                                     |                                                                                              |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                    |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                               |
| Namespace<br/>                | Root\\StandardCimv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>NetAdapterCim.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>NetAdapterCim.dll</dt> </dl> |



 

 



