# 说明

这里是目录和进度。

[TOC]

## 0. Core

即核心着色器。

| 文档名                         | 文档进度 | 原理解析文档 | 翻译者 |
| ------------------------------ | -------- | ------------ | ------ |
| AdjustTranslucentFS            |          |              |        |
| BillboardCollectionFS          |          |              |        |
| BillboardCollectionVS          |          |              |        |
| BrdfLutGeneratorFS             |          |              |        |
| CompareAndPackTranslucentDepth |          |              |        |
| CompositeOITFS                 |          |              |        |
| DepthPlaneFS                   |          |              |        |
| DepthPlaneVS                   |          |              |        |
| EllipsoidFS                    |          |              |        |
| EllipsoidVS                    |          |              |        |
| GlobeFS                        |          |              |        |
| GlobeVS                        |          |              |        |
| GroundAtmosphere               |          |              |        |
| OctahedralProjectionAtlasFS    |          |              |        |
| OctahedralProjectionFS         |          |              |        |
| OctahedralProjectionVS         |          |              |        |
| PointPrimitiveCollectionFS     |          |              |        |
| PointPrimitiveCollectionVS     |          |              |        |
| PolylineCommon                 |          |              |        |
| PolylineFS                     |          |              |        |
| PolylineShadowVolumeFS         |          |              |        |
| PolylineShadowVolumeMorphFS    |          |              |        |
| PolylineShadowVolumeMorphVS    |          |              |        |
| PolylineShadowVolumeVS         |          |              |        |
| PolylineVS                     |          |              |        |
| ReprojectWebMercatorFS         |          |              |        |
| ReprojectWebMercatorVS         |          |              |        |
| ShadowVolumeAppearanceFS       |          |              |        |
| ShadowVolumeAppearanceVS       |          |              |        |
| ShadowVolumeFS                 |          |              |        |
| SkyAtmosphereCommon            |          |              |        |
| SkyAtmosphereFS                |          |              |        |
| SkyAtmosphereVS                |          |              |        |
| SkyBoxFS                       |          |              |        |
| SkyBoxVS                       |          |              |        |
| SunFS                          |          |              |        |
| SunTextureFS                   |          |              |        |
| SunVS                          |          |              |        |
| Vector3DTileClampedPolylinesFS |          |              |        |
| Vector3DTileClampedPolylinesVS |          |              |        |
| Vector3DTilePolylinesVS        |          |              |        |
| VectorTileVS                   |          |              |        |
| ViewportQuadFS                 |          |              |        |
| ViewportQuadVS                 |          |              |        |



## 1. Appearances/

| 文档名                           | 文档进度 | 原理解析文档 | 翻译者 |
| -------------------------------- | -------- | ------------ | ------ |
| AllMaterialAppearanceFS          |          |              |        |
| AllMaterialAppearanceVS          |          |              |        |
| BasicMaterialAppearanceFS        |          |              |        |
| BasicMaterialAppearanceVS        |          |              |        |
| EllipsoidSurfaceAppearanceFS     |          |              |        |
| EllipsoidSurfaceAppearanceVS     |          |              |        |
| PerInstanceColorAppearanceFS     |          |              |        |
| PerInstanceColorAppearanceVS     |          |              |        |
| PerInstanceFlatColorAppearanceFS |          |              |        |
| PerInstanceFlatColorAppearanceVS |          |              |        |
| PolylineColorAppearanceVS        |          |              |        |
| PolylineMaterialAppearanceVS     |          |              |        |
| TexturedMaterialAppearanceFS     |          |              |        |
| TexturedMaterialAppearanceVS     |          |              |        |



## 2. Builtin/



### 2.1. Constants/

| 文档名 | 文档进度 | 原理解析文档 | 翻译者 |
| ------ | -------- | ------------ | ------ |
| degreesPerRadian                         |      |      |      |
| depthRange                               |      |      |      |
| epsilon[1~7]                             |      |      |      |
| infinity                                 |      |      |      |
| oneOverPi                                |      |      |      |
| oneOverTwoPi                             |      |      |      |
| passCesium3DTile                         |      |      |      |
| passCesium3DTileClassification           |      |      |      |
| passCesium3DTileClassificationIgnoreShow |      |      |      |
| passClassification                       |      |      |      |
| passCompute                              |      |      |      |
| passEnvironment                          |      |      |      |
| passGlobe                                |      |      |      |
| passOpaque                               |      |      |      |
| passOverlay                              |      |      |      |
| passTerrainClassification                |      |      |      |
| passTranslucent                          |      |      |      |
| pi & piOver[Four/Six/Three/Two]          |      |      |      |
| radiansPerDegree                         |      |      |      |
| sceneMode[2D/3D/ColumbusView/Morphing]   |      |      |      |
| solarRadius                              |      |      |      |
| threePiOver2                             |      |      |      |
| twoPi                                    |      |      |      |
| webMercatorMaxLatitude                   |      |      |      |



### 2.2. Functions/

| 文档名                                                    | 文档进度           | 原理解析文档 | 翻译者   |
| --------------------------------------------------------- | ------------------ | ------------ | -------- |
| acesTonemapping                                           |                    |              |          |
| alphaWeight                                               |                    |              |          |
| antialias                                                 |                    |              |          |
| approximateSphericalCoordinates                           |                    |              |          |
| backFacing                                                |                    |              |          |
| branchFreeTernary                                         |                    |              |          |
| cascadeColor                                              |                    |              |          |
| cascadeDistance                                           |                    |              |          |
| cascadeMatrix                                             |                    |              |          |
| cascadeWeights                                            |                    |              |          |
| columbusViewMorph                                         |                    |              |          |
| computePosition                                           |                    |              |          |
| cosineAndSine                                             |                    |              |          |
| decompressTextureCoordinates                              |                    |              |          |
| defaultPbrMaterial                                        |                    |              |          |
| depthClamp                                                |                    |              |          |
| eastNorthUpToEyeCoordinates                               |                    |              |          |
| ellipsoidContainsPoint                                    |                    |              |          |
| ellipsoidWgs84TextureCoordinates                          |                    |              |          |
| equalsEpsilon                                             |                    |              |          |
| eyeOffset                                                 |                    |              |          |
| eyeToWindowCoordinates                                    |                    |              |          |
| fastApproximateAtan                                       |                    |              |          |
| fog                                                       |                    |              |          |
| gammaCorrect                                              |                    |              |          |
| geodeticSurfaceNormal                                     |                    |              |          |
| getDefaultMaterial                                        |                    |              |          |
| getLambertDiffuse                                         |                    |              |          |
| getSpecular                                               |                    |              |          |
| getWaterNoise                                             |                    |              |          |
| HSBToRGB                                                  |                    |              |          |
| HSLToRGB                                                  |                    |              |          |
| hue                                                       |                    |              |          |
| inverseGamma                                              |                    |              |          |
| isEmpty                                                   |                    |              |          |
| isFull                                                    |                    |              |          |
| latitudeToWebMercatorFraction                             |                    |              |          |
| lineDistance                                              |                    |              |          |
| luminance                                                 |                    |              |          |
| metersPerPixel                                            |                    |              |          |
| modelToWindowCoordinates                                  |                    |              |          |
| multiplyWithColorBalance                                  |                    |              |          |
| nearFarScalar                                             |                    |              |          |
| octDecode                                                 |                    |              |          |
| packDepth                                                 |                    |              |          |
| pbrLighting                                               |                    |              |          |
| pbrMetallicRoughnessMaterial                              |                    |              |          |
| pbrSpecularGlossinessMaterial                             |                    |              |          |
| phong                                                     |                    |              |          |
| [planeDistance](./Builtin/Functions/planeDistance.md)     | ing                | 缺少         | onsummer |
| pointAlongRay                                             |                    |              |          |
| rayEllipsoidIntersectionInterval                          |                    |              |          |
| [readDepth](./Builtin/Functions/readDepth.md)             | :white_check_mark: | 不需要       | onsummer |
| readNonPerspective                                        |                    |              |          |
| [reverseLogDepth](./Builtin/Functions/reverseLogDepth.md) | :white_check_mark: | 缺少         | onsummer |
| RGBToHSB                                                  |                    |              |          |
| RGBToHSL                                                  |                    |              |          |
| RGBToXYZ                                                  |                    |              |          |
| sampleOctahedralProjection                                |                    |              |          |
| saturation                                                |                    |              |          |
| shadowDepthCompare                                        |                    |              |          |
| shadowVisibility                                          |                    |              |          |
| signNotZero                                               |                    |              |          |
| sphericalHarmonics                                        |                    |              |          |
| tangentToEyeSpaceMatrix                                   |                    |              |          |
| transformPlane                                            |                    |              |          |
| translateRelativeToEye                                    |                    |              |          |
| traslucentPhong                                           |                    |              |          |
| transpose                                                 |                    |              |          |
| unpackDepth                                               |                    |              |          |
| unpackFloat                                               |                    |              |          |
| vertexLogDepth                                            |                    |              |          |
| windowToEyeCoordinates                                    |                    |              |          |
| writeDepthClamp                                           |                    |              |          |
| writeLogDepth                                             |                    |              |          |
| writeNonPerspective                                       |                    |              |          |
| XYZToRGB                                                  |                    |              |          |



### 2.3. Structs/

| 文档名                                                    | 文档进度           | 原理解析文档 | 翻译者   |
| --------------------------------------------------------- | ------------------ | ------------ | -------- |
| [depthRangeStruct](./Builtin/Structs/depthRangeStruct.md) | :white_check_mark: | 不需要       | onsummer |
| [material](./Builtin/Structs/material.md)                 | :white_check_mark: | 不需要       | onsummer |
| [materialInput](./Builtin/Structs/materialInput)          | ing                | 不需要       | onsummer |
| [pbrParameters](./Builtin/Structs/pbrParameters.md)       | ing                | 不需要       | onsummer |
| [ray](./Builtin/Structs/ray.md)                           | :white_check_mark: | 不需要       | onsummer |
| [raySegment](./Builtin/Structs/raySegment.md)             | ing                | 不需要       | onsummer |
| [shadowParameters](./Builtin/Structs/shadowParameters.md) | ing                | 缺少         | onsummer |



## 3. Materials/

| 文档名                  | 文档进度 | 原理解析文档 | 翻译者 |
| ----------------------- | -------- | ------------ | ------ |
| AspectRampMaterial      |          |              |        |
| BumpMapMaterial         |          |              |        |
| CheckerboardMaterial    |          |              |        |
| DotMaterial             |          |              |        |
| ElevationBandMaterial   |          |              |        |
| ElevationRampMaterial   |          |              |        |
| FadeMaterial            |          |              |        |
| GridMaterial            |          |              |        |
| NormalMapMaterial       |          |              |        |
| PolylineDashMaterial    |          |              |        |
| PolylineGlowMaterial    |          |              |        |
| PolylineOutlineMaterial |          |              |        |
| RimLightingMaterial     |          |              |        |
| SlopeRampMaterial       |          |              |        |
| StripeMaterial          |          |              |        |
| Water                   |          |              |        |



## 4. PostProcessStages/

| 文档名                             | 文档进度 | 原理解析文档 | 翻译者 |
| ---------------------------------- | -------- | ------------ | ------ |
| AcesTonemappingStage               |          |              |        |
| AdditiveBlend                      |          |              |        |
| AmbientOcclusionGenerate           |          |              |        |
| AmbientOcclusionModulate           |          |              |        |
| BlackAndWhite                      |          |              |        |
| BloomComposite                     |          |              |        |
| Brightness                         |          |              |        |
| BrightPass                         |          |              |        |
| CompositeTranslucentClassification |          |              |        |
| ContrastBias                       |          |              |        |
| DepthOfField                       |          |              |        |
| DepthView                          |          |              |        |
| DepthViewPacked                    |          |              |        |
| EdgeDetection                      |          |              |        |
| FilmicTonemapping                  |          |              |        |
| FXAA                               |          |              |        |
| GaussianBlur1D                     |          |              |        |
| LensFlare                          |          |              |        |
| ModifiedReinhardTonemapping        |          |              |        |
| NightVision                        |          |              |        |
| PassThrough                        |          |              |        |
| PassThroughDpeth                   |          |              |        |
| PointCloudEyeDomeLighting          |          |              |        |
| ReinhardTonemapping                |          |              |        |
| Slihouette                         |          |              |        |

# TODO

- AutomaticUniforms
- Primitive Builtin Shader
