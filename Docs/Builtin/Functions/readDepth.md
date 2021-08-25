# 源代码

``` glsl
float czm_readDepth(sampler2D depthTexture, vec2 texCoords)
{
    return czm_reverseLogDepth(texture2D(depthTexture, texCoords).r);
}
```

# 文档

一个函数，从深度纹理中根据纹理坐标，取深度值。

## 1. 参数

### ① depthTexture

参数类型：`sampler2D`

深度纹理。

### ② texCoords

参数类型：`vec2`

纹理坐标。

## 2. 返回值

返回值类型：`float`



# 注意事项

`depthTexture` 可以是对数深度纹理，也可以是非对数深度纹理。



# 参考

函数：[czm_reverseLogDepth](./reverseLogDepth.md)

