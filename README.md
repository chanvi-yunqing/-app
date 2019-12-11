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
 
#### 人体关键点识别

- 当上传的图片较为清晰，图片中的人物仅为一人时，API可以清晰明了的返回图像数据，根据图片人物的特性，API可以精确的返回21个关键点数据，此API可以精准定位人体的21个主要关键点，包含头顶、五官、颈部、四肢主要关节部位；支持人体背面、侧面、中低空斜拍、大动作等复杂场景

- 当上传的图片较为清晰，但是图片中的人物较多时，API只可以识别图片中间的人物，图片边缘的人物不能够精准的识别到，甚至会发现识别得不到的情况，以下图片为7人照片，使用该API人体关键点检测的功能识别图片只能识别5个人物的关键点，数据返回也较为详细准确，但是位于边缘的两位人物API并不能完全识别出人物的关键点数据，甚至在最右侧的人物出现了完全不能识别的现象。
![API测试2](https://images.gitee.com/uploads/images/2019/1210/230556_da0a6f11_1648233.png "测试2.png")

- 当上传的图片较为模糊，但是图片人物数量较少时，百度API的人体关键点识别功能依然可以较为准确的识别出人体的关键点，返回的数据相对来说也较为准确，上传图片后，API需要2~3秒的扫描时长后才能返回出图片数据。

#### 人体检测与属性识别

- 百度API中的人体检测与属性识别可以识别人体的20余类通用属性，包含性别年龄、服饰类别、服饰颜色、佩戴物、行为动作（抽烟/使用手机等），但是返回的数据结果较为简单，相对于其他API的人脸识别功能来说相对较弱一点，在上传图片后，系统需要扫描5~6秒的时间才能返回数据结果，扫描时间较长，长时间的等待会影响到一部分使用者的用户体验，以下图片为返回的文字结果
![文字结果](https://images.gitee.com/uploads/images/2019/1211/140249_1c6d2cec_1648233.png "返回文字结果.png")


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

### 信息设计

### 原型文档

## API 产品使用关键AI或机器学习之API的输出入展示

### API使用水平

- 百度API人体关键点分析接口描述：对于输入的一张图片（可正常解码，且长宽比适宜），检测图片中的所有人体，输出每个人体的21个主要关键点，包含头顶、五官、脖颈、四肢等部位，同时输出人体的坐标信息和数量。支持多人检测、人体位置重叠、遮挡、背面、侧面、中低空俯拍、大动作等复杂场景。21个关键点的位置：头顶、左耳、右耳、左眼、右眼、鼻子、左嘴角、右嘴角、脖子、左肩、右肩、左手肘、右手肘、左手腕、右手腕、左髋部、右髋部、左膝、右膝、左脚踝、右脚踝。

- 输入：上传图片获取关键点信息

```
# encoding:utf-8

import requests
import base64

'''
人体关键点识别
'''

request_url = "https://aip.baidubce.com/rest/2.0/image-classify/v1/body_analysis"
# 二进制方式打开图片文件
f = open('[本地文件]', 'rb')
img = base64.b64encode(f.read())

params = {"image":img}
access_token = '[调用鉴权接口获取的token]'
request_url = request_url + "?access_token=" + access_token
headers = {'content-type': 'application/x-www-form-urlencoded'}
response = requests.post(request_url, data=params, headers=headers)
if response:
    print (response.json())
    
```

- 输入图片如下
![API测试图片1](https://images.gitee.com/uploads/images/2019/1210/230120_3e22d224_1648233.png "5f0208412f292d5b12ff75e61e5a589.png")

ps：在使用以上输入代码时必须先获取token，使用示例代码前，请记得替换其中的示例Token、图片地址或Base64信息
具体获取token的方法请看
[百度API获取token的方法](https://ai.baidu.com/ai-doc/REFERENCE/Ck3dwjhhu)

- 人体关键点分析输出结果示意图

```
{
	"person_num": 2,
	"person_info": [
		{
			"body_parts": {
				"left_hip": {
					"y": 573,
					"x": 686.09375,
					"score": 0.78743487596512
				},
				"top_head": {
					"y": 242.53125,
					"x": 620,
					"score": 0.87757384777069
				},
				"right_mouth_corner": {
					"y": 308.625,
					"x": 606.78125,
					"score": 0.90121293067932
				},
				"neck": {
					"y": 335.0625,
					"x": 620,
					"score": 0.84662038087845
				},
				"left_shoulder": {
					"y": 361.5,
					"x": 699.3125,
					"score": 0.83550786972046
				},
				"left_knee": {
					"y": 731.625,
					"x": 699.3125,
					"score": 0.83575332164764
				},
				"left_ankle": {
					"y": 877.03125,
					"x": 725.75,
					"score": 0.85220056772232
				},
				"left_mouth_corner": {
					"y": 308.625,
					"x": 633.21875,
					"score": 0.91475087404251
				},
				"right_elbow": {
					"y": 348.28125,
					"x": 461.375,
					"score": 0.81766486167908
				},
				"right_ear": {
					"y": 282.1875,
					"x": 593.5625,
					"score": 0.86551451683044
				},
				"nose": {
					"y": 295.40625,
					"x": 620,
					"score": 0.90894532203674
				},
				"left_eye": {
					"y": 282.1875,
					"x": 633.21875,
					"score": 0.89628517627716
				},
				"right_eye": {
					"y": 282.1875,
					"x": 606.78125,
					"score": 0.89676940441132
				},
				"right_hip": {
					"y": 586.21875,
					"x": 593.5625,
					"score": 0.79803824424744
				},
				"left_wrist": {
					"y": 374.71875,
					"x": 884.375,
					"score": 0.89635348320007
				},
				"left_ear": {
					"y": 295.40625,
					"x": 659.65625,
					"score": 0.86607384681702
				},
				"left_elbow": {
					"y": 361.5,
					"x": 791.84375,
					"score": 0.83910942077637
				},
				"right_shoulder": {
					"y": 348.28125,
					"x": 553.90625,
					"score": 0.85635334253311
				},
				"right_ankle": {
					"y": 890.25,
					"x": 580.34375,
					"score": 0.85149073600769
				},
				"right_knee": {
					"y": 744.84375,
					"x": 580.34375,
					"score": 0.83749794960022
				},
				"right_wrist": {
					"y": 348.28125,
					"x": 368.84375,
					"score": 0.83893859386444
				}
			},
			"location": {
				"height": 703.20654296875,
				"width": 652.61810302734,
				"top": 221.92272949219,
				"score": 0.99269664287567,
				"left": 294.03039550781
			}
		},
		{
			"body_parts": {
				"left_hip": {
					"y": 576,
					"x": 1239.5625,
					"score": 0.84608125686646
				},
				"top_head": {
					"y": 261.15625,
					"x": 1176.59375,
					"score": 0.871442258358
				},
				"right_mouth_corner": {
					"y": 336.71875,
					"x": 1164,
					"score": 0.90951544046402
				},
				"neck": {
					"y": 361.90625,
					"x": 1176.59375,
					"score": 0.85904294252396
				},
				"left_shoulder": {
					"y": 361.90625,
					"x": 1239.5625,
					"score": 0.8512310385704
				},
				"left_knee": {
					"y": 714.53125,
					"x": 1277.34375,
					"score": 0.82312393188477
				},
				"left_ankle": {
					"y": 853.0625,
					"x": 1315.125,
					"score": 0.83786374330521
				},
				"left_mouth_corner": {
					"y": 336.71875,
					"x": 1189.1875,
					"score": 0.90610301494598
				},
				"right_elbow": {
					"y": 387.09375,
					"x": 1025.46875,
					"score": 0.88956367969513
				},
				"right_ear": {
					"y": 311.53125,
					"x": 1138.8125,
					"score": 0.86518502235413
				},
				"nose": {
					"y": 324.125,
					"x": 1176.59375,
					"score": 0.9168484210968
				},
				"left_eye": {
					"y": 311.53125,
					"x": 1189.1875,
					"score": 0.91715461015701
				},
				"right_eye": {
					"y": 311.53125,
					"x": 1164,
					"score": 0.90343600511551
				},
				"right_hip": {
					"y": 576,
					"x": 1164,
					"score": 0.81976848840714
				},
				"left_wrist": {
					"y": 298.9375,
					"x": 1378.09375,
					"score": 0.86095398664474
				},
				"left_ear": {
					"y": 311.53125,
					"x": 1201.78125,
					"score": 0.86899447441101
				},
				"left_elbow": {
					"y": 324.125,
					"x": 1315.125,
					"score": 0.89198768138885
				},
				"right_shoulder": {
					"y": 387.09375,
					"x": 1101.03125,
					"score": 0.85161662101746
				},
				"right_ankle": {
					"y": 878.25,
					"x": 1151.40625,
					"score": 0.83667933940887
				},
				"right_knee": {
					"y": 727.125,
					"x": 1151.40625,
					"score": 0.85485708713531
				},
				"right_wrist": {
					"y": 387.09375,
					"x": 949.90625,
					"score": 0.83042001724243
				}
			},
			"location": {
				"height": 670.80139160156,
				"width": 524.25476074219,
				"top": 241.42504882812,
				"score": 0.98725789785385,
				"left": 902.15216064453
			}
		}
	],
	"log_id": "6362401025381690607"
}
```

- 以上输出内容为输入一张静态图片后输出了结果，结果包括了人体21个关键点的分析
- body_parts，一共21个part，每个part包含x，y两个坐标，如果part被截断，则x、y坐标为part被截断的图片边界位置，part顺序以实际返回顺序为准。
- 接口返回人体坐标框和每个关键点的置信度分数，在应用时可综合置信度score分数，过滤掉置信度低的“无效人体”，建议过滤方法：当关键点得分大于0.2的个数大于3，且人体框的分数大于0.03时，才认为是有效人体。实际应用中，可根据对误识别、漏识别的容忍程度，调整阈值过滤方案，灵活应用。

#### 人体检测与属性识别（输入与输出）

- 当输入上传图片时
```
# encoding:utf-8

import requests
import base64

'''
人体检测和属性识别
'''

request_url = "https://aip.baidubce.com/rest/2.0/image-classify/v1/body_attr"

# 二进制方式打开图片文件

f = open('[本地文件]', 'rb')
img = base64.b64encode(f.read())

params = {"image":img}
access_token = '[调用鉴权接口获取的token]'
request_url = request_url + "?access_token=" + access_token
headers = {'content-type': 'application/x-www-form-urlencoded'}
response = requests.post(request_url, data=params, headers=headers)
if response:
    print (response.json())
```
以下为输入图片
![输入图片](https://images.gitee.com/uploads/images/2019/1211/141047_816e8958_1648233.jpeg "输入图片.jpg")

-输出结果为以下数据
```
{
	"person_num": 1,
	"person_info": [
		{
			"attributes": {
				"upper_wear_fg": {
					"score": 0.82246553897858,
					"name": "衬衫"
				},
				"cellphone": {
					"score": 0.99057698249817,
					"name": "未使用手机"
				},
				"lower_cut": {
					"score": 0.85645776987076,
					"name": "有下方截断"
				},
				"umbrella": {
					"score": 0.99916100502014,
					"name": "未打伞"
				},
				"orientation": {
					"score": 0.99120199680328,
					"name": "正面"
				},
				"is_human": {
					"score": 0.98832511901855,
					"name": "正常人体"
				},
				"headwear": {
					"score": 0.79590553045273,
					"name": "无帽"
				},
				"gender": {
					"score": 0.58045083284378,
					"name": "男性"
				},
				"age": {
					"score": 0.9393767118454,
					"name": "青年"
				},
				"upper_cut": {
					"score": 0.99673992395401,
					"name": "无上方截断"
				},
				"glasses": {
					"score": 0.42270773649216,
					"name": "无眼镜"
				},
				"lower_color": {
					"score": 0.86391562223434,
					"name": "白"
				},
				"bag": {
					"score": 0.83722245693207,
					"name": "无背包"
				},
				"upper_wear_texture": {
					"score": 0.4370131790638,
					"name": "纯色"
				},
				"smoke": {
					"score": 0.99516922235489,
					"name": "未吸烟"
				},
				"vehicle": {
					"score": 0.9986184835434,
					"name": "无交通工具"
				},
				"lower_wear": {
					"score": 0.86400103569031,
					"name": "不确定"
				},
				"carrying_item": {
					"score": 0.73127031326294,
					"name": "无手提物"
				},
				"upper_wear": {
					"score": 0.91392177343369,
					"name": "长袖"
				},
				"occlusion": {
					"score": 0.99049419164658,
					"name": "无遮挡"
				},
				"upper_color": {
					"score": 0.98802477121353,
					"name": "白"
				}
			},
			"location": {
				"height": 936,
				"width": 591,
				"top": 16,
				"score": 0.99892431497574,
				"left": 60
			}
		}
	],
	"log_id": "6881378423438836555"
}
```

### API使用比较分析

- 一下为两家人体关键点识别API的对比与检测，这两家家技术平台分别是，face++，百度API，仅有这两家平台提供人体检测API

|   平台  | 功能    |  特性  |  返回结果   |  返回时间   |
| --- | --- | --- | --- | --- |
| face++    | 人体关键点    |   定位并返回人体各部位关键点坐标位置。关键点定位了头、颈、肩、肘、手、臀、膝、脚等部位，但仅能识别较少的关键点 |仅能分析15个人体关键点，且没有具体数据   |  1s   |
|  百度API   |  人体关键点 |   对于输入的一张图片（可正常解码，且长宽比适宜），检测图片中的所有人体，输出每个人体的21个主要关键点，包含头顶、五官、脖颈、四肢等部位，同时输出人体的坐标信息和数量。支持多人检测、人体位置重叠、遮挡、背面、侧面、中低空俯拍、大动作等复杂场景。21个关键点的位置：头顶、左耳、右耳、左眼、右眼、鼻子、左嘴角、右嘴角、脖子、左肩、右肩、左手肘、右手肘、左手腕、右手腕、左髋部、右髋部、左膝、右膝、左脚踝、右脚踝。  | body_parts，一共21个part，每个part包含x，y两个坐标，如果part被截断，则x、y坐标为part被截断的图片边界位置，part顺序以实际返回顺序为准。接口返回人体坐标框和每个关键点的置信度分数，在应用时可综合置信度score分数，过滤掉置信度低的“无效人体”，建议过滤方法：当关键点得分大于0.2的个数大于3，且人体框的分数大于0.03时，才认为是有效人体。实际应用中，可根据对误识别、漏识别的容忍程度，调整阈值过滤方案，灵活应用。    | 2s    |

- 根据实际的API功能检测显示，face++的人体识别功能主要反馈线框数据为主，识别的关键点仅为15个，虽然反馈结果的时间较短但是数据识别的功能相对比较弱；
- 百度API人体关键点是被可以识别的关键点为21个，当上传一张较为清晰的个人图时，可以在2秒之内扫描完图片并输出相应的数据，数据的精确度较高，但是在上传一张多人图时，能识别的人数较为不齐全，中间的人群可以较精准的识别，但是在图片边缘的人识别率较低甚至识别不了。
- 总结：根据以上的检测分析，我们决定使用百度API的人体关键点分析技术，相较下百度API的共嫩比较符合我们的预期。

### 使用后风险报告

#### API市场竞争程度

- 根据资料查询显示，现有较大的API平台中拥有人体关键点分析功能的API平台仅有两家分别时face++和百度API，而百度API中的功能相对face++来说较为齐全也比较智能，百度API中的人体关键点分析可以根据人体关键点信息，分析人体姿态、运动轨迹、动作角度等，辅助运动员进行体育训练，分析健身锻炼效果，提升教学效率，比较适合我们产品的API选择，而face++相对来说关键点识别数量较少，精准度较低，但是对于动态的视频精准度较高，face++平台的专注点比较偏向于人脸识别和人脸对比的功能，在识别人脸的功能中face++比百度API的功能更加智能，返回的数据也更加的齐全，但是针对人体关键点分析这一项功能，百度API所返回的数据更加的精确，数据更加的齐全，百度API中所提供的技术相对来说较为广，发展完善的速度也比较快，在API市场竞争中所占的优势较大。

#### 输入输出限制

- 请求限制：请求图片需经过base64编码：图片的base64编码指将一副图片数据编码成一串字符串，使用该字符串代替图像地址。我们可以首先得到图片的二进制，然后用Base64格式编码即可。

- 请求格式支持：PNG、JPG、BMP

- 图片编码后大小限额：base64编码后进行urlencode，要求base64编码和urlencode后大小不超过4M，最短边至少50px，最长边最大4096px ，建议长宽比3：1以内

- 请求参数限制：图像数据，base64编码后进行urlencode，要求base64编码和urlencode后大小不超过4M。图片的base64编码是不包含图片头的，如(data:image/jpg;base64,)，支持图片格式：jpg、bmp、png，最短边至少50px，最长边最大4096px

- 返回结果：接口除了返回人体框和每个关键点的坐标信息外，还会输出人体框和关键点的概率分数，实际应用中可以基于概率分数进行过滤，排除掉分数低的误识别“无效人体”，推荐的过滤方案：当关键点得分大于0.2的个数大于3，且人体框的得分大于0.03时，才认为是有效人体。实际应用中，可根据对误识别、漏识别的容忍程度，调整阈值过滤方案，灵活应用，比如对误识别容忍低的应用场景，人体框的得分阈值可以提到0.05甚至更高。

- 返回参数分析：接口返回人体坐标框和每个关键点的置信度分数，在应用时可综合置信度score分数，过滤掉置信度低的“无效人体”，建议过滤方法：当关键点得分大于0.2的个数大于3，且人体框的分数大于0.03时，才认为是有效人体。

#### 定价

- 按QPS（并发量）计费： 调用量免费，免费QPS默认为2，如果您通过百度云的企业认证，接口的免费QPS将扩充至5。同时您可以根据业务需求随时购买扩充QPS，QPS可包月购买，也可按天单独购买，灵活多样，适应多场景需求。 当前人体关键点识别、人体检测与属性识别、人流量统计、人像分割、手势识别5个接口支持在线购买QPS。 注意：同一个账号下多个应用共享接口QPS。
- 按调用量计费： 免费调用量限额用完后，可选择购买次数包 或开通 按调用量后付费 两种计费方式付费使用，两种付费方式均可在 控制台 直接开通或购买，开通付费后默认按量后付费的方式进行阶梯计费，如有购买对应服务的次数包，则优先消耗次数包额度，抵扣完毕后自动转为按量后付费方式。 当前驾驶行为分析接口采用按调用量计费的方式。

- 免费额度

![免费额度](https://images.gitee.com/uploads/images/2019/1211/114821_96da938e_1648233.png "免费额度.png")

- 按QPS付费
当前人体关键点识别、人体检测与属性识别、人流量统计、人像分割、手势识别5个接口支持在线购买QPS。购买QPS后，无论是否通过企业认证，调用量额度都会升级为无限制。

![定价](https://images.gitee.com/uploads/images/2019/1211/115009_813ca7e1_1648233.png "定价.png")

具体定价请查看[百度API人体关键点分析定价](https://ai.baidu.com/ai-doc/BODY/mk3cpyhfe)

### 加分项

- 用到百度API人体关键点识别，人体检测与人脸属性API，具体调用如下显示：


