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
