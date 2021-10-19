# 源代码

``` glsl
vec4 czm_windowToEyeCoordinates(vec4 fragmentCoordinate)
{
  // 窗口坐标重建NDC坐标
  float x = 2.0 * (fragmentCoordinate.x - czm_viewport.x) / czm_viewport.z - 1.0;
  float y = 2.0 * (fragmentCoordinate.y - czm_viewport.y) / czm_viewport.w - 1.0;
  float z = (fragmentCoordinate.z - czm_viewportTransformation[3][2]) / czm_viewportTransformation[2][2];
  vec4 q = vec4(x, y, z, 1.0);

  // NDC坐标转裁剪（投影）坐标
  q /= fragmentCoordinate.w;

  // 裁剪（投影）坐标转y（相机）坐标
  if (!(czm_inverseProjection == mat4(0.0))) // IE and Edge sometimes do something weird with != between mat4s
  {
    q = czm_inverseProjection * q;
  }
  else
  {
    float top = czm_frustumPlanes.x;
    float bottom = czm_frustumPlanes.y;
    float left = czm_frustumPlanes.z;
    float right = czm_frustumPlanes.w;

    float near = czm_currentFrustum.x;
    float far = czm_currentFrustum.y;

    q.x = (q.x * (right - left) + left + right) * 0.5;
    q.y = (q.y * (top - bottom) + bottom + top) * 0.5;
    q.z = (q.z * (near - far) - near - far) * 0.5;
    q.w = 1.0;
  }

  return q;
}

vec4 czm_windowToEyeCoordinates(vec2 fragmentCoordinateXY, float depthOrLogDepth)
{
  // See reverseLogDepth.glsl. This is separate to re-use the pow.
#ifdef LOG_DEPTH
  float near = czm_currentFrustum.x;
  float far = czm_currentFrustum.y;
  float log2Depth = depthOrLogDepth * czm_log2FarDepthFromNearPlusOne;
  float depthFromNear = pow(2.0, log2Depth) - 1.0;
  float depthFromCamera = depthFromNear + near;
  vec4 windowCoord = vec4(fragmentCoordinateXY, far * (1.0 - near / depthFromCamera) / (far - near), 1.0);
  vec4 eyeCoordinate = czm_windowToEyeCoordinates(windowCoord);
  eyeCoordinate.w = 1.0 / depthFromCamera; // Better precision
  return eyeCoordinate;
#else
  vec4 windowCoord = vec4(fragmentCoordinateXY, depthOrLogDepth, 1.0);
  vec4 eyeCoordinate = czm_windowToEyeCoordinates(windowCoord);
#endif
  return eyeCoordinate;
}
```

# 文档

该函数能将窗口坐标计算至眼坐标（也即相机坐标、观察坐标）。有两个重载。

## 1. 参数

### 重载1 ① fragmentCoordinate

参数类型：`vec4`

片元的窗口坐标。

### 重载2 ① fragmentCoordinateXY

参数类型：`vec2`

片元的窗口坐标，二维。

### 重载2 ② depthOrLogDepth

参数类型：`float`

（对数）深度值。



## 2. 返回值

返回值类型：`vec4`



# 注意事项

`depthTexture` 可以是对数深度纹理，也可以是非对数深度纹理。


