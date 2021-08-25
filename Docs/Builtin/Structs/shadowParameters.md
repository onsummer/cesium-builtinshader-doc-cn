# 源代码

``` glsl
struct czm_shadowParameters
{
#ifdef USE_CUBE_MAP_SHADOW
    vec3 texCoords;
#else
    vec2 texCoords;
#endif

    float depthBias;
    float depth;
    float nDotL;
    vec2 texelStepSize;
    float normalShadingSmooth;
    float darkness;
};
```

# 文档

## 1. 成员 `texCoords`

### 类型

当宏 `USE_CUBE_MAP_SHADOW` 定义时，为 `vec3`；

否则为 `vec2`.

### 说明

TODO.



## 2. 成员 `depthBias`

### 类型

`float`



## 3. 成员 `depth`

### 类型

`float`



## 4. 成员 `nDotL`

### 类型

`float`



## 5. 成员 `texelStepSize`

### 类型

`vec2`



## 6. 成员 `normalShadingSmooth`

### 类型

`float`



## 7. 成员 `darkness`

### 类型

`float`