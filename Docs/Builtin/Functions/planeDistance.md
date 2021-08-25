# 源代码

``` glsl
float czm_planeDistance(vec4 plane, vec3 point) {
    return (dot(plane.xyz, point) + plane.w);
}

float czm_planeDistance(vec3 planeNormal, float planeDistance, vec3 point) {
    return (dot(planeNormal, point) + planeDistance);
}
```

