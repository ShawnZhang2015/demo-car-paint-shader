# 车漆着色器 / Car Paint Shader

写实风格的汽车金属漆着色器通用模板，可适用于各类汽车展示。

## 注意事项
![image.png](https://download.cocos.com/Cocos/CocosStore/markdown/2022/01/da6c3d68c78152439fe6b9c0219f277587454.png)

**本资源仅含着色器代码，不含用于演示的汽车模型，汽车模型请移步链接下载**：

[https://www.cgtrader.com/3d-models/car/standard/realistic-car-hd-02](https://www.cgtrader.com/3d-models/car/standard/realistic-car-hd-02)

## 功能介绍
- 写实风格的汽车金属漆着色器
- 着色器提供的美术效果包括：色漆层、清漆层、金属颗粒、橘皮、菲涅尔反射
- 建议在 Cocos Creator 3.4.0 以及以上版本中使用
- 资源包包含内容：Effect文件、测试材质、测试场景


## 操作说明
- 将 builtin-standard-carpaint.effect 拷贝到 Cocos Creator 项目文件中
- 创建一个新材质，Effect 选择 builtin-standard-carpaint.effect
- 着色器包含所有 Cocos Creator 标准 PBR 流程的功能，可依照 PBR 工作流使用
- 勾选 USE CLEARCOAT，开启清漆层
- （可选）在 Clear Coat Normal Map 中输入橘皮法线贴图
- （可选）在 Reflection Environment Map 中输入环境反射 HDR 贴图
- （可选）在 Reflection Lighting Map 中输入第二章环境反射贴图，用于制作 HDR 光照效果
- 勾选 USE FLAKE，开启金属颗粒
- （可选）在 Flake Mask Map 中输入金属颗粒遮罩贴图
- （可选）在 Flake Normal Map 中输入金属颗粒法线贴图
- Second Paint Color：第二套色漆颜色，仅在观察角度为掠射角的部分着色
- Fresnel Scale：控制菲涅尔反射强度
- Fresnel Hardness：控制菲涅尔反射范围
- Reflection(1) Albedo(0) Scalar：在有使用环境反射贴图的前提下，调和反射颜色和固有色的权重，1 = 反射颜色100%；0 = 固有色100%
- Reflection Scale：环境反射贴图的强度（环境反射将依据菲涅尔反射的效果实现）
- Reflection Hardness：环境反射贴图的范围（环境反射将依据菲涅尔反射的效果实现）
- Reflection Lighting Scale: 第二张环境反射贴图（HDR光照）的强度
- CoatTiling：橘皮法线贴图的 UV tiling
- Clear Coat Normal Scale：橘皮的法线强度
- FlakeTiling：金属颗粒贴图的 UV tiling
- Flake Size：金属颗粒的大小（效果与 UV tiling 相同）
- Flake Distance：金属颗粒的深度（数值较大时，金属颗粒在越远的距离仍然可见）
- Flake Normal Scale：金属颗粒的法线强度

## 使用教程
- 依照色漆层的美术需求，使用标准 PBR 功能制作色漆层效果
- 调节菲涅尔数值，配合第二套色漆颜色参数调节菲涅尔效果
- 使用 Metallic 值调节金属漆/非金属漆，可以获得相应的高光溢出效果
- 开启 USE FLAKE，调节金属颗粒的密度和大小，配合色漆层的高光观察效果
- 开启 USE CLEARCOAT，使用环境反射贴图制作清漆层的反光效果
- 依照项目需求，使用第二张 HDR 贴图输入Reflection Lighting Map 参数，可以配合 HDR Light Studio 等 DCC 制作特定的 studio lighting 效果
- 继续配合调节菲涅尔强度和反射强度，对整体效果进行把控

## 效果展示
![scr_01.jpg](https://download.cocos.com/Cocos/CocosStore/markdown/2022/01/14b005b2ce8f1b749b7f102eb1c31e3d54643.jpg)
![scr_02.jpg](https://download.cocos.com/Cocos/CocosStore/markdown/2022/01/1c590a2da4b22bd947001678094cd3fd62895.jpg)
![scr_03.jpg](https://download.cocos.com/Cocos/CocosStore/markdown/2022/01/2267e872dc01a14ff28bf7377653171f60962.jpg)