---
title: IStillImage RefreshDeviceBus method
description: The IStillImage GetSTILaunchInformation method is used to request a bus refresh.
ms.assetid: a89f2eeb-db02-4d68-91f9-5a922c740b83
keywords:
- RefreshDeviceBus method Still Image
- RefreshDeviceBus method Still Image , IStillImage interface
- IStillImage interface Still Image , RefreshDeviceBus method
topic_type:
- apiref
api_name:
- IStillImage.RefreshDeviceBus
api_type:
- COM
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IStillImage::RefreshDeviceBus method

The [**IStillImage::GetSTILaunchInformation**](https://www.bing.com/search?q=**IStillImage::GetSTILaunchInformation**) method is used to request a bus refresh.

## Syntax


```C++
HRESULT RefreshDeviceBus(
  [in] LPCWSTR pwszDeviceName
);
```



## Parameters

<dl> <dt>

*pwszDeviceName* \[in\]
</dt> <dd>

The friendly device name of the device to reset

</dd> </dl>

## Return value

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Remarks

This method is mainly used for non PnP buses like SCSI, whe the device was powered on after PnP enumeration.

## See also

<dl> <dt>

[**IStillImage**](https://www.bing.com/search?q=**IStillImage**)
</dt> </dl>

 

 



