---
title: SampleGrad(S,float,float,float,int,float) function
description: Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.
ms.assetid: CBC940D5-FC09-498D-9C7A-3CBAB2EC2D4D
keywords:
- SampleGrad function HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# SampleGrad(S,float,float,float,int,float) function

Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.

## Syntax


```C++
DXGI_FORMAT SampleGrad(
  _In_ SamplerState S,
  _In_ float        Location,
  _In_ float        DDX,
  _In_ float        DDY,
  _In_ int          Offset,
  _In_ float        Clamp
);
```



## Parameters

<dl> <dt>

*S* \[in\]
</dt> <dd>

Type: **SamplerState**

A [Sampler state](dx-graphics-hlsl-sampler.md). This is an object declared in an effect file that contains state assignments.

</dd> <dt>

*Location* \[in\]
</dt> <dd>

Type: **float**

The texture coordinates. The argument type is dependent on the texture-object type.



| Texture-Object Type                    | Parameter Type |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*DDX* \[in\]
</dt> <dd>

Type: **float**

The rate of change of the surface geometry in the x direction. The argument type is dependent on the texture-object type.



| Texture-Object Type                      | Parameter Type |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | not supported  |



 

</dd> <dt>

*DDY* \[in\]
</dt> <dd>

Type: **float**

The rate of change of the surface geometry in the y direction. The argument type is dependent on the texture-object type.



| Texture-Object Type                      | Parameter Type |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | not supported  |



 

</dd> <dt>

*Offset* \[in\]
</dt> <dd>

Type: **int**

An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling. Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware. The argument type is dependent on the texture-object type. For more info, see [Applying Integer Offsets](https://www.bing.com/search?q=Applying Integer Offsets).



| Texture-Object Type           | Parameter Type |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | not supported  |



 

</dd> <dt>

*Clamp* \[in\]
</dt> <dd>

Type: **float**

An optional value to clamp sample LOD values to. For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.

</dd> </dl>

## Return value

Type: **[**DXGI\_FORMAT**](https://msdn.microsoft.com/library/windows/desktop/bb173059)**

The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](https://msdn.microsoft.com/library/windows/desktop/bb173059).

## See also

<dl> <dt>

[SampleGrad methods](texture2darray-samplegrad.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 



