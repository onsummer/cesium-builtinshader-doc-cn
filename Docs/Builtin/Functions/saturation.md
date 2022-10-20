# 源代码

```glsl
/**
 * Adjusts the saturation of a color.
 * 
 * @name czm_saturation
 * @glslFunction
 * 
 * @param {vec3} rgb The color.
 * @param {float} adjustment The amount to adjust the saturation of the color.
 *
 * @returns {float} The color with the saturation adjusted.
 *
 * @example
 * vec3 greyScale = czm_saturation(color, 0.0);
 * vec3 doubleSaturation = czm_saturation(color, 2.0);
 */
vec3 czm_saturation(vec3 rgb, float adjustment)
{
    // Algorithm from Chapter 16 of OpenGL Shading Language
    const vec3 W = vec3(0.2125, 0.7154, 0.0721);
    vec3 intensity = vec3(dot(rgb, W));
    return mix(intensity, rgb, adjustment);
}
```

# 文档

调整颜色值（RGB格式）的饱和度，使用《OpenGL Shading Language》第 16 章中提及的饱和度调整算法：

- 使用权重向量 `vec3(0.2125, 0.7154, 0.0721)` 点乘 RGB 颜色向量，得到一个灰度值

- 将此灰度值与原来的 RGB 颜色进行 `mix` 混合，混合插值系数是 `adjustment`

- 返回一个调整饱和度后的颜色值 `vec3`

可以简单理解为入参 `adjustment` 就是调整饱和度的系数，值的范围是 `[0, 1]`


