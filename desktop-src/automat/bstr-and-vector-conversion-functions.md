---
title: BSTR and Vector Conversion Functions
description: Automation supports conversion between an array of bytes and a BSTR through the two low-level conversion functions VectorFromBstr and BstrFromVector, and by performing the appropriate conversions in VariantChangeType, ITypeInfo Invoke, DispInvoke, and other relevant locations.
ms.assetid: 482c0e05-2841-446a-a2d0-015ae55c806e
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# BSTR and Vector Conversion Functions

Automation supports conversion between an array of bytes and a BSTR through the two low-level conversion functions [**VectorFromBstr**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-vectorfrombstr) and [**BstrFromVector**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-bstrfromvector), and by performing the appropriate conversions in [**VariantChangeType**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-variantchangetype), [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke), [**DispInvoke**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-dispinvoke), and other relevant locations.

BSTRs are wide, double-byte (Unicode) strings on 32-bit Windows platforms, and narrow, single-byte strings on 16-bit Windows and the Apple PowerMac. These functions do not perform any special string handling. They simply move bytes from one location to another, so the width of strings does not affect these API functions.

## In this section



| Topic                                               | Description                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**BstrFromVector**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-bstrfromvector)<br/> | Returns a BSTR, assigning each element of the vector to a character in the BSTR.<br/>    |
| [**SetOaNoCache**](setoanocache.md)<br/>     | Disables the **BSTR** caching in OleAut32.dll. <br/>                                     |
| [**VarBstrCat**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-varbstrcat)<br/>         | Concatenates two variants of type BSTR and returns the resulting BSTR.<br/>              |
| [**VarBstrCmp**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-varbstrcmp)<br/>         | Compares two variants of type BSTR.<br/>                                                 |
| [**VectorFromBstr**](/previous-versions/windows/desktop/api/OleAuto/nf-oleauto-vectorfrombstr)<br/> | Returns a vector, assigning each character in the BSTR to an element of the vector.<br/> |



 

> [!Note]  
> If these functions are passed NULL pointers, there will be an access violation and the program will crash. It is your responsibility to protect these functions against NULL pointers.

 

## Related topics

<dl> <dt>

[Conversion and Manipulation Functions](conversion-and-manipulation-functions.md)
</dt> </dl>

 

 




