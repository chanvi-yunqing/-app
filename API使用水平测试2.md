
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
