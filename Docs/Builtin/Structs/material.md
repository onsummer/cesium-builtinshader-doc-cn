# 源代码

``` glsl
/**
 * Holds material information that can be used for lighting. Returned by all czm_getMaterial functions.
 *
 * @name czm_material
 * @glslStruct
 *
 * @property {vec3} diffuse Incoming light that scatters evenly in all directions.
 * @property {float} specular Intensity of incoming light reflecting in a single direction.
 * @property {float} shininess The sharpness of the specular reflection.  Higher values create a smaller, more focused specular highlight.
 * @property {vec3} normal Surface's normal in eye coordinates. It is used for effects such as normal mapping. The default is the surface's unmodified normal.
 * @property {vec3} emission Light emitted by the material equally in all directions. The default is vec3(0.0), which emits no light.
 * @property {float} alpha Opacity of this material. 0.0 is completely transparent; 1.0 is completely opaque.
 */
struct czm_material
{
    vec3 diffuse;
    float specular;
    float shininess;
    vec3 normal;
    vec3 emission;
    float alpha;
};
```

# 文档

材质信息，一般使用 `czm_getMaterial` 函数来创建。

## 1. 成员 `diffuse`

### 类型

`vec3`

### 含义

漫反射入射光。



## 2. 成员 `specular`

### 类型

`float`

### 含义

入射光强度。



## 3. 成员 `shininess`

### 类型

`float`

### 含义

镜面反射强度。高值会产生更明显的镜面高光效果。



## 4. 成员 `normal`

### 类型

`vec3`

### 含义

观察坐标系（eye-coordinate）中的法向量。



## 5. 成员 `emission`

### 类型

`vec3`

### 含义

自发光色。默认值是 `vec3(0.0)`，即不发光。



## 6. 成员 `alpha`

### 类型

`float`

### 含义

材质的透明度。0.0 是完全透明，1.0 是完全不透明。





# 参考

- `czm_getMaterial` 函数