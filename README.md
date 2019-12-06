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


## 第二部分：产品原型

