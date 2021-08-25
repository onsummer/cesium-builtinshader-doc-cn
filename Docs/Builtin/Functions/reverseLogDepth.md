# 源代码

``` glsl
float czm_reverseLogDepth(float logZ)
{
#ifdef LOG_DEPTH
    float near = czm_currentFrustum.x;
    float far = czm_currentFrustum.y;
    float log2Depth = logZ * czm_log2FarDepthFromNearPlusOne;
    float depthFromNear = pow(2.0, log2Depth) - 1.0;
    return far * (1.0 - near / (depthFromNear + near)) / (far - near);
#endif
    return logZ;
}
```

# 文档

一个函数，将对数深度值解算到普通的深度值。

## 1. 参数

### ① logZ

参数类型：`float` 

对数深度值。

## 2. 返回值

返回值类型：`float`

普通深度值。



# 原理

TODO.
