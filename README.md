# 教你说产品文档

文档信息|详细内容|
---|---|
发布日期|2019-12|
产品名称|教你说APP|
文档现状|进行中
主人|赖绮薇

# 一、核心价值主张
## 1. 加值宣言

## 2. 核心价值（最小可行性产品）

本产品旨在为学龄前儿童提供更好的英汉双语口语教学服务，通过如拍照识图进行学习等**趣味的方式、标准的语音**来引导学龄前儿童进行口语学习，减轻父母教学的压力，保障教学质量。同时用户可根据自身学习情况选择相对应的学习内容，并跟随本平台所提供的教学方案进行口语学习。
## 3. 核心价值与用户痛点

近年来，教育一直呈现**低龄化**的现象，许多父母会在孩子很小的时候就为孩子报上不少兴趣班，希望孩子可以赢在起跑线。但在对兴趣班进行选择的时候，家长通常无法对其进行质量筛选，通常都是通过朋友推荐的方式选择。而“教你说”这个平台则能减去家长的时间成本，直接提供**高质量的教学内容**及**趣味的教学方式**，让孩子在玩耍中学习，**保持孩子探索世界的好奇心**。
## 4. AI概率性与用户痛点

作为父母，为孩子报兴趣班的目的自然在于希望得到优质教学，如口语教学类平台，用户希望获得的便是标准的发音教学。尽管目前的AI语音合成技术发展飞快，但仍存在着一定不流畅不自然的现象。因此在教学过程中，存在着用户**误把尚未完善的发音当作标准发音**的可能，并进行学习，对平台有一定的信任风险。
## 5. 需求列表与API加值

需求功能|重要程度|API支持|
---|---|---|
标准双语发音|非常重要|语音合成
识别物体|次重要|图片识别
返回评分|一般重要|语音识别、语音合成

# 二、原型设计

![启动页](https://images.gitee.com/uploads/images/2019/1225/105244_4744e340_1831468.jpeg "start.jpeg")

![首页](https://images.gitee.com/uploads/images/2019/1225/105259_097085d4_1831468.jpeg "first.jpeg")

![训练营](https://images.gitee.com/uploads/images/2019/1225/105342_17d74d8d_1831468.jpeg "xunlian.jpeg")

![详情](https://images.gitee.com/uploads/images/2019/1225/105517_3864302d_1831468.jpeg "xiangqing.jpeg")

![闯关](https://images.gitee.com/uploads/images/2019/1225/105530_16a57726_1831468.jpeg "chuang.jpeg")

![趣味模式](https://images.gitee.com/uploads/images/2019/1225/105546_978a8f2d_1831468.jpeg "quwei.jpeg")

![拍照](https://images.gitee.com/uploads/images/2019/1225/105604_6b8f1f04_1831468.jpeg "camera.jpeg")

![上传](https://images.gitee.com/uploads/images/2019/1225/105624_d8191ffc_1831468.jpeg "photo.jpeg")

![识别成功](https://images.gitee.com/uploads/images/2019/1225/105638_5cfcff4e_1831468.jpeg "yes.jpeg")

![识别失败](https://images.gitee.com/uploads/images/2019/1225/105653_f59ec5ad_1831468.jpeg "no.jpeg")

![更多](https://images.gitee.com/uploads/images/2019/1225/105704_64c607c2_1831468.jpeg "more.jpeg")

# 三、API应用

## 1.API调用
### 图像识别
#### 百度开放平台

![百度通用识别](https://images.gitee.com/uploads/images/2019/1223/162354_ac1d52b4_1831468.png "baidu_pic.png")

参考文档：[百度通用物体和场景识别API参考文档](https://ai.baidu.com/ai-doc/IMAGERECOGNITION/Xk3bcxe21)  

### 语音合成
#### 百度开放平台

![百度语音合成](https://images.gitee.com/uploads/images/2019/1223/220503_cfe64486_1831468.png "baidu_speaking.png")

参考文档：[百度语音识别API参考文档](https://ai.baidu.com/ai-doc/SPEECH/2k38y8iut)  
代码示例：[官方示例](https://github.com/Baidu-AIP/speech-demo/blob/master/rest-api-tts/python/tts.py)

## 2.API对比分析

### 语音合成
#### (1)功能分析

API类别|所属平台|功能|优劣分析|
---|---|---|---|
语音合成|谷歌||英文发音较为标准|
语音合成|百度|让文字“发声”|仅有9种音库，4种音色，但支持多音字标注，中文发音标准|
在线语音合成|科大讯飞|将文字信息转换为语音信息|个性化定制，多达18种多语种及多方言，还可选择场景及音色年龄段|

参考文档：
[百度语音合成文档](https://ai.baidu.com/tech/speech/tts)

[科大讯飞语音合成文档](https://www.xfyun.cn/services/online_tts)

#### (2)价格分析

a. 百度

![百度语音收费表](https://images.gitee.com/uploads/images/2019/1221/112633_83dff83f_1831468.jpeg "百度价格.jpg")

参考文档：[百度在线语音合成计费说明](http://ai.baidu.com/ai-doc/SPEECH/Nk38y8pjq)

b. 科大讯飞

![科大讯飞语音收费表](https://images.gitee.com/uploads/images/2019/1221/113048_0bda2e10_1831468.jpeg "科大讯飞价格.jpg")

参考文档：[科大讯飞在线语音合成](http://www.xfyun.cn/services/online_tts)

### 图片识别
#### 

#### (1)功能分析

API类别|所属平台|功能|优劣分析
---|---|---|---|
通用物体和场景识别|百度|识别物体和场景名称，获取百科信息|识别后返回结果较为详细，有相关解释及分类|
图片识别|腾讯|看图说话、多标签识别、模糊图片识别、美食图片识别、物体/场景识别|只能将图片信息转换为文本信息，同时返回内容不够详细|

参考文档：
[百度通用物体和场景识别文档](https://ai.baidu.com/tech/imagerecognition/general)  
[腾讯图片识别文档](https://ai.qq.com/product/visionimgidy.shtml#express)

#### (2)价格分析

a. 百度

![百度图像识别价格表](https://images.gitee.com/uploads/images/2019/1223/225536_cb5ac708_1831468.png "baidu_pic.png")

参考文档：[百度通用物体和场景识别定价文档](https://ai.baidu.com/ai-doc/IMAGERECOGNITION/gk3bcx9n1)

b. 腾讯

未找到价格相关文档。

### 总结
1. 从功能上来说，**百度开放平台**的图像识别API返回信息较为全面，并且支持多种物体识别，同时百度开放平台提供了植物识别、动物识别、地标识别、果蔬识别等全方位多功能的API，识别范围覆盖较广；**腾讯开放平台**的看图说话功能，虽返回结果是以一句话的形式呈现，但返回的信息较少，不够全面。
2. 在使用语音合成API的过程中，经比较发现**科大讯飞平台**的功能及可选音色、语种较多，较为注重细节方面，同时发音标准，与人类音调较为相像；**百度开放平台**提供选择的音色不多，且语种较为单一，同时仍存在着发音别扭的情况，但其平台文档内容提供到位，使用体验尚佳。
3. 总体而言，**腾讯开放平台**个人使用感一般般，其图像识别API及语音合成API并没有过人之处，并且没有相关的价格文档，技术性文档提供内容也不足。
