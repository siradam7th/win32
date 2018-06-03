---
Description: Sets blending event keys for the specified animation track.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: ID3DXAnimationController::KeyPriorityBlend method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXAnimationController::KeyPriorityBlend method

Sets blending event keys for the specified animation track.

## Syntax


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## Parameters

<dl> <dt>

*NewBlendWeight* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Number between 0 and 1 that is used to blend tracks together.

</dd> <dt>

*StartTime* \[in\]
</dt> <dd>

Type: **[**DOUBLE**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Global time to start the blend.

</dd> <dt>

*Duration* \[in\]
</dt> <dd>

Type: **[**DOUBLE**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Global time duration of the blend.

</dd> <dt>

*Transition* \[in\]
</dt> <dd>

Type: **[**D3DXTRANSITION\_TYPE**](https://msdn.microsoft.com/windows/desktop/4416ef28-ba6b-47ca-be7d-831daad619e5)**

Specifies the transition type used for the duration of the blend. See [**D3DXTRANSITION\_TYPE**](https://msdn.microsoft.com/windows/desktop/4416ef28-ba6b-47ca-be7d-831daad619e5).

</dd> </dl>

## Return value

Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Event handle to the priority blend event. **NULL** is returned if one or more of the input parameters is invalid, or no free event is available.

## Remarks

The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 



