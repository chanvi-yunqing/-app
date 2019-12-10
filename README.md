## 懂你所动——运动智能APP

|  发布日期   |  2019.12   |
| --- | --- |
|  项目名称   |  懂你所动   |
|  文件主人   |  陈蕴晴   |
|  领头设计者 |  陈蕴晴   |
|  领头开发者 |  陈蕴晴   |
|  领头测试者 |  陈蕴晴   |

## 第一部分：PRD价值主张设计

### 背景概述
- 近几年来减肥热充斥着我们的日常生活，人们为了追求更完美的身材逐渐开始关注运动健身，但是不少人刚开始健身时没有完全了解自己的身体状况，盲目的运动健身导致付出了时间但收效甚差。针对这一现象我们想推出一款智能运动app叫“懂你所动”。

### 产品介绍——价值宣言
- 懂你所动智能运动app用户通过上传正面全身照，侧面全身照和背面全身照，系统通过人体关键点监测和人体监测与属性的分析，反馈给用户自身相应的身体体型数据，系统会根据用户的数据推荐一些与用户身体形态相对应的健身视频给用户，用户在开始运动的时可以打开手机的摄像功能持续拍摄用户的健身视频，系统会根据用户上传的视频通过人体关键点分析，根据人体关键点信息，分析人体姿态、运动轨迹、动作角度等，来识别系统推荐给用户的运动视频是否符合用户自身的身体状况，并根据数据适当的调节推荐视频的难度。

### 产品核心价值
- 现阶段日益增多的减肥和塑性的人群因为对自身体型的认知度不高，盲目的运动健身导致付出了时间但收效小，甚至会在运动的过程中受伤，针对这一现象懂你所动智能运动app可以根据用户上传的全身照或者视频来识别用户身体形态的数据，系统根据用户的数据推荐适合用户的健身视频和健身教程，提高用户健身的效率同时降低用户在运动过程中受伤的可能性。

### 核心价值与用户痛点
- 针对体型肥胖者，运动健身者，塑型减肥者，运动小白，在刚开始运动时对健身的认知度较低，对自己的身体状况和身形体态的认知度不足，由于种种原因导致用户无法正确的选择适合自己的运动视频和运动教程，盲目的选择教程会使得用户健身事倍功半。

### 需求列表与人工智能API价值
| 用户 | 场景需求 | 重要程度 |
| --- | --- | --- |
| 体型肥胖者 | 开始减肥却不知道从哪里开始减肥，同时不知道用什么方法减肥 | 重要 |
| 塑性减肥者 | 身材比例较差，身材略显畸形，不知道自己的身材那一部分出现了问题 | 重要 |
| 运动小白   | 刚开始运动健身，但是不知道应该怎么锻炼才是适合自己 | 重要 |

- 人工智能API价值体现：百度AI中的人体关键点监测API的功能可以检测图像中的人体并返回人体矩形框位置，精准定位21个核心关键点，包含头顶、五官、颈部、四肢主要关节部位，支持多人检测、大动作等复杂场景，检测图像中的所有人体，标记出每个人体的坐标位置；不限人体数量，适应人体轻度遮挡、截断的情况，在用户运动健身的时候可以根据人体关键点信息，分析人体姿态、运动轨迹、动作角度等，辅助运动员进行体育训练，分析健身锻炼效果，提升教学效率，这一功能技术是懂你所动APP的核心技术与核心功能，根据用户上传的图片和视频信息反馈出用户数据，系统根据用户信息给用户推荐适合用户的运动教程和运送视频。

### 人工智能概率性与用户痛点
- 图像中人物数量较少，且上传照片清晰度较高
![API测试图片1](https://images.gitee.com/uploads/images/2019/1210/230120_3e22d224_1648233.png "5f0208412f292d5b12ff75e61e5a589.png")

- 图像人物数量较多时，上传图片的清晰度较高但是人物在图片中所占比较小
![API测试2](https://images.gitee.com/uploads/images/2019/1210/230556_da0a6f11_1648233.png "测试2.png")

- 图像人物较少，且上传图片较为模糊
![API测试3](https://images.gitee.com/uploads/images/2019/1210/231158_546ec163_1648233.png "测试3.png")

- 从上图所显示出的数据中，我们可以看出当图像人物较少时且图片上传清晰度较高的铧话，API识别出的数据较为齐全，基本满足我们APP的技能的需求，而当图像人物数量较多时且上传图片的清晰度较高时，API中识别中的人物不齐全，第二章图片中有7个人，但是能够真正识别完整的就只有5个人，所以百度API针对多人的图片识别相对较弱；当图像人物较少，且上传的图片较为模糊，API所识别的关键点相对来说也时较为齐全的，基本可以满足我们APP的需求。

## 第二部分：产品原型

### 产品框架示意图

![产品框架](https://images.gitee.com/uploads/images/2019/1210/232011_b6aec5f5_1648233.png "在这里输入图片标题")

### 产品核心功能图片

![产品核心技术](https://images.gitee.com/uploads/images/2019/1210/232143_f2028083_1648233.png "产品核心功能图.png")

### 产品使用流程图
![流程图](https://images.gitee.com/uploads/images/2019/1210/232429_c9da968f_1648233.jpeg "懂你所动流程图.jpg")

### 交互及界面设计
![交互界面](https://images.gitee.com/uploads/images/2019/1211/002434_dca55427_1648233.png "交互界面.png")

- 上图所示为APP首页中的数据检测板块，用户通过上传自己的全身照，然后系统利用2~3秒的时间进行扫描得出用户的数据并将检测到的数据反馈给用户，原型如上图所示，该检测功能使用了人体关键点识别的API功能，精准定位人体的21个主要关键点，包含头顶、五官、颈部、四肢主要关节部位；支持人体背面、侧面、中低空斜拍、大动作等复杂场景，通过上传图片扫描后得出第二章图的数据，该数据包括了21个关键点的数据。
