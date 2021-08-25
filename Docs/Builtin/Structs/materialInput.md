# 源代码

``` glsl
/**
 * Used as input to every material's czm_getMaterial function.
 *
 * @name czm_materialInput
 * @glslStruct
 *
 * @property {float} s 1D texture coordinates.
 * @property {vec2} st 2D texture coordinates.
 * @property {vec3} str 3D texture coordinates.
 * @property {vec3} normalEC Unperturbed surface normal in eye coordinates.
 * @property {mat3} tangentToEyeMatrix Matrix for converting a tangent space normal to eye space.
 * @property {vec3} positionToEyeEC Vector from the fragment to the eye in eye coordinates.  The magnitude is the distance in meters from the fragment to the eye.
 * @property {float} height The height of the terrain in meters above or below the WGS84 ellipsoid.  Only available for globe materials.
 * @property {float} slope The slope of the terrain in radians.  0 is flat; pi/2 is vertical.  Only available for globe materials.
 * @property {float} aspect The aspect of the terrain in radians.  0 is East, pi/2 is North, pi is West, 3pi/2 is South.  Only available for globe materials.
 */
struct czm_materialInput
{
    float s;
    vec2 st;
    vec3 str;
    vec3 normalEC;
    mat3 tangentToEyeMatrix;
    vec3 positionToEyeEC;
    float height;
    float slope;
    float aspect;
};
```

# 文档

## 1. 成员 `s`

### 类型

`float`

### 含义

一维纹理坐标



## 2. 成员 `st`

### 类型

`vec2`

### 含义

二维纹理坐标



## 3. 成员 `str`

### 类型

`vec3`

### 含义

三维纹理坐标



## 4. 成员 `normalEC`

### 类型

`vec3`

### 含义

观察坐标（eye-coordinate，EC）中的法向量。



## 5. 成员 `tangentToEyeMatrix`

### 类型

`mat3`



## 5. 成员 `positionToEyeEC`

### 类型

`vec3`



## 6. 成员 `height`

### 类型

`float`



## 7. 成员 `slope`

### 类型

`float`



## 8. 成员 `aspect`

### 类型

`float`
