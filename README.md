### 智能毕业相册

|   产品名字  |  Moments   |
| --- | --- |
|    文件主人 |   陈蕴晴  |
|    文件设计者 |  陈蕴晴   |



### Moments APP产品背景（价值宣言）
- 随着智能生活的普及，人们生活品质的上升，人们越来越习惯使用手机记录生活琐碎的细节，市场上出现了具有各种各样拍照修图功能的APP，但是市场上却缺乏照片智能整理的APP，用户缺乏一个能够智能整理照片和资料的相册；Moments APP就是一款打造全新智能生活的智能毕业相册，这款APP以face++ API为技术支撑服务平台，它不仅可以帮助用户整理照片打造一个智能相册，还可以根据用户图片中的表情和姿势给照片中的任务亲密程度和开心程度打分，Moments智能相册可以识别每张照片中的任务并根据图像之间的人脸分析把同一个朋友圈子的任务照片进行相册归类。

### 智能毕业相册核心价值（最小可用产品）

- 智能毕业相册人像识别功能：智能相册app中有个人像识别功能，相册可以识别相片中的人物，在每张相片中出现人物信息的提示功能。

- 亲密程度测试：智能相册app可以根据相片中人物之间的站位，表情动作给图片中的人物打亲密程度的分数和人物的开心指数。

- 识别人物分类相册：智能相册app可以识别每张照片的人物并根据图像之间的人脸分析把同一圈子的人物照片进行相册的归类。


### 智能毕业相册核心价值与用户痛点
- 随着社会的发展，人们生活方式的改变，人们越来越喜欢使用手机拍照记录生活，但是面对手机相册中多而杂乱的图片，用户又应该如何去归类呢？有这个问题困扰的群体会希望能够出现以款智能整理照片的相册，可以帮助用户把手机中杂乱的照片进行归类整理。


### 目标市场分析
- 随着社会的发展，现阶段社会中国智能手机普及率为68%，处于中游水平，而在这68%中，年轻人占据绝大部分；现阶段人们喜欢使用智能手机的拍照功能记录生活琐碎的瞬间，随着社会对拍照软件的需求，市场上出现了各种各样的智能拍照APP，拍照功能的APP在是市场中逐渐趋于饱和的状态，但是相对应的现在逐渐衍生出了智能相册的APP软件，但现阶段智能相册APP还处初创阶段，市场并没有完全打开，在这个还没有完全成熟的市场中Moments智能相册的推出可以更好的抢占市场的先机，吸引更多年轻的用户使用我们智能相册


### 目标用户

- 在校就读学生

- 喜欢拍照记录生活的人群

- 手机中储存了许多照片的人群

### 使用场景（需求列表）

#### 场景一
- 小明是一名刚刚大学毕业的大学生，在毕业当天他和大学的同学和老师拍了许多的照片，回到家里小明想要编辑图片发朋友圈却发现朋友圈智能够一次发9张图片，而小明又不想使用拼图软件把图片拼起来；后来他在APP store中发现了Moments APP，在这里他发现可以直接把手机相册和APP连接后app可以智能识别毕业当天的照片，并根据照片中的人物，场所进行分类排序和整理，每张照片还可以智能识别出朋友之间的亲密程度和开心程度，甚至小明可以编辑图片中人物的资料后，app通过人脸识别到该人物出现的每一张照片中都可以储存相应的人物资料。

#### 场景二
- 小红是一名旅游爱好者，在这一年内小红去了几个地方旅游，一天她查看之前旅游的照片，但是发现手机相册中的照片太过于凌乱，她希望能有个软件可以帮助她整理相册中的相片，后来她在APP store中发现了Moments APP，在这里她可以根据自己的喜好分类相片，比如她在关键字框中输入“北京”，智能相册app马上可以识别出小红在北京这个地方所拍的照片并根据时间和地点有序的排列好照片，点击照片还可以弹出照片中的场景定位和拍照时间。

### 产品核心价值（最小可用产品）——用户痛点
- 想要通过智能分类手机照片，将手机中杂乱的照片整齐有序可以按照自己喜好去排版好一个个相册的用户群体，以往手机自带的相册功能智能按照时间顺序去排列相片，用户在查找照片的时候需要一张张的去翻看，需要花费用户较长的时间去寻找目标照片，他们迫切希望有智能分类识别功能的app提供给他们使用。

### API&AI选择

- face++ [人脸API](https://www.faceplusplus.com.cn/face-detection/)

#### Azure人脸API功能介绍(需求列表与人工智能API价值）
1. 人脸识别
Face++ 提供了人脸检测、83个关键点检测与跟踪、人脸分析、1:1 人脸比对或 1:N 人脸搜索的能力。开发者在此基础上做进一步开发，即可轻松实现美颜、面部贴图、身份验证、任务识别、照片聚类等功能。

2. 证件识别
利用 Face++ 的 OCR 技术，开发者的产品可以识别出身份证、驾照、行驶证上的文字，快速采集证件内的文本信息。

3. 图像识别
利用 Face++ 的图像识别技术，开发者的产品可以识别出图片中的文字、场景和物体。

### API使用水平
- 输入图片
```
//人脸比对
- (void)sessionCompare{
    NSString *urlStr = @"https://api-cn.faceplusplus.com/facepp/v3/compare";
    NSURL *url = [NSURL URLWithString:urlStr];
    NSMutableURLRequest *request = [NSMutableURLRequest requestWithURL:url];
    request.HTTPMethod = @"POST";
    NSString *contentType = [NSString stringWithFormat:@"multipart/form-data; boundary=%@",@"boundary"];
    [request setValue:contentType forHTTPHeaderField:@"Content-Type"];
    NSDictionary *dict = @{@"api_key" : @"xxxxxxxxxxxxx",//你的api_key
                           @"api_secret" : @"xxxxxxxxxxxxx",//你的api_secret
                          };
    NSString *path1 = [[NSBundle mainBundle] pathForResource:@"image1" ofType:@"jpeg"];
    NSString *path2 = [[NSBundle mainBundle] pathForResource:@"image2" ofType:@"jpeg"];
    NSData *data1 = [NSData dataWithContentsOfFile:path1];
    NSData *data2 = [NSData dataWithContentsOfFile:path2];
    
    ///////////////////////NSURLSession 示例如下:
    NSData *bodyData = [self bodyDataWithParam:dict fileData:@[@{@"fieldName" : @"image_file1" ,@"data" : data1 , @"fileType" : @"jpeg"},@{@"fieldName" : @"image_file2" ,@"data" : data2 , @"fileType" : @"jpeg"}]];
    NSURLSessionTask *task = [[NSURLSession sharedSession] uploadTaskWithRequest:request fromData:bodyData completionHandler:^(NSData * _Nullable data, NSURLResponse * _Nullable response, NSError * _Nullable error) {
        if (error) {
            NSLog(@"%@",error);
        }else{
            id obj = [NSJSONSerialization JSONObjectWithData:data options:NSJSONReadingMutableContainers error:nil];
            NSLog(@"%@",[obj class]);
            NSLog(@"%@",obj);
        }
    }];
    [task resume];
    
    ///////////////////////NSURLConnection 示例如下:
    /*
    request.HTTPBody = bodyData;
    [NSURLConnection sendAsynchronousRequest:request queue:[NSOperationQueue new] completionHandler:^(NSURLResponse * _Nullable response, NSData * _Nullable data, NSError * _Nullable connectionError) {
        if (connectionError) {
            NSLog(@"%@",connectionError);
        }else{
            id obj = [NSJSONSerialization JSONObjectWithData:data options:NSJSONReadingMutableContainers error:nil];
            NSLog(@"%@",[obj class]);
            NSLog(@"%@",obj);
        }
    }];
    */
}
- (NSData *)bodyDataWithParam:(NSDictionary *)param fileData:(NSArray<NSDictionary *> *)fileDatas{
    NSMutableData *bodyData = [NSMutableData data];
    //拼接参数
    [param enumerateKeysAndObjectsUsingBlock:^(id  _Nonnull key, id  _Nonnull obj, BOOL * _Nonnull stop) {
        [bodyData appendData:[@"--boundary\r\n" dataUsingEncoding:NSUTF8StringEncoding]];
        [bodyData appendData:[[NSString stringWithFormat:@"Content-Disposition: form-data; name=\"%@\"\r\n\r\n",key] dataUsingEncoding:NSUTF8StringEncoding]];
        [bodyData appendData:[[NSString stringWithFormat:@"%@\r\n",obj] dataUsingEncoding:NSUTF8StringEncoding]];
    }];
    //拼接文件二进制数据
    for (NSDictionary *dic in fileDatas) {
        NSString *fieldName = dic[@"fieldName"];
        NSData *fileData = dic[@"data"];
        NSString *fileType = dic[@"fileType"];
        [bodyData appendData:[@"--boundary\r\n" dataUsingEncoding:NSUTF8StringEncoding]];
        [bodyData appendData:[[NSString stringWithFormat:@"Content-Disposition: form-data; name=\"%@\"; filename=\"%@\"\r\n", fieldName, fieldName] dataUsingEncoding:NSUTF8StringEncoding]];
        [bodyData appendData:[[NSString stringWithFormat:@"Content-Type: %@\r\n\r\n", fileType] dataUsingEncoding:NSUTF8StringEncoding]];
        [bodyData appendData:fileData];
        [bodyData appendData:[@"\r\n" dataUsingEncoding:NSUTF8StringEncoding]];
    }
    [bodyData appendData:[@"--boundary--\r\n" dataUsingEncoding:NSUTF8StringEncoding]];
    return bodyData;
    
}
```
- 输出结果
```
{
    "image_id": "Dd2xUw9S/7yjr0oDHHSL/Q==", 
    "request_id": "1470472868,dacf2ff1-ea45-4842-9c07-6e8418cea78b", 
    "time_used": 752, 
    "faces": [
        {
            "landmark": {
                "mouth_upper_lip_left_contour2": {
                    "y": 185, 
                    "x": 146
                }, 
                "contour_chin": {
                    "y": 231, 
                    "x": 137
                }, 
               .........省略关键点信息
                "right_eye_pupil": {
                    "y": 146, 
                    "x": 205
                }, 
                "mouth_upper_lip_bottom": {
                    "y": 195, 
                    "x": 159
                }
            }, 
            "attributes": {
                "gender": {
                    "value": "Female"
                }, 
                "age": {
                    "value": 21
                }, 
                "glass": {
                    "value": "None"
                }, 
                "headpose": {
                    "yaw_angle": -26.625063, 
                    "pitch_angle": 12.921974, 
                    "roll_angle": 22.814377
                }, 
                "smile": {
                    "threshold": 30.1, 
                    "value": 2.566890001296997
                }
            }, 
            "face_rectangle": {
                "width": 140, 
                "top": 89, 
                "left": 104, 
                "height": 141
            }, 
            "face_token": "ed319e807e039ae669a4d1af0922a0c8"
        }
    ]
}
```
1. API
通过 API 直接调用 Face++ 的各项能力，适合联网产品。

2. SDK
移动端应用通过嵌入SDK获得开放能力，适合离线场景（如实时美颜），目前支持 Android / iOS。

- *人脸检测：* 检测并定位图片中的人脸，返回高精度的人脸框坐标。Face++还支持存储检测到的人脸元数据，以便日后使用。
- *人脸对比：* 计算两张脸的相似程度，并给出相似度评分，以便分析属于一个人的可能性。
- *人脸搜索：* 针对一个新的人脸，在一个已有的人脸集合中搜索相似的人脸。算法会返回一系列相似人脸，以及相似度评分。
- *人脸分组：* 组 API 会基于相似性将未知人脸的集合分为几组。 每个组是原始人脸集合的互不相交真子集。 一个组中的所有人脸可能属于同一人。 一个人可能有多个不同的组。 组按其他因素（例如表情）区分。
- *人脸关键点：* 定位并返回人脸五官与轮廓的关键点坐标位置。关键点包括人脸轮廓、眼睛、眉毛、嘴唇以及鼻子轮廓。
- *人脸情绪：* 分析检测到的人脸的情绪，并返回置信度分数。目前 Face++ 能够识别愤怒、厌恶、恐惧、高兴、平静、伤心、惊讶等七类情绪。
- *人脸属性：* 进行一系列人脸相关的属性分析，包括年龄、性别、头部朝向、情绪、颜值、视线、皮肤状态等属性。

立即体验
（具体操作内容请看[人脸API](https://www.faceplusplus.com.cn/face-detection/））

### API使用风险报告（人工智能概率性与用户痛点）
- 一开始我想使用Azure的人脸识别API来完成这一毕业相册的API提供者，但是在网上的资料显示和其他用用户的使用反馈后，因为微软只能达到17.55%的人脸检测率，图片数据集中的确有一些故意刁难识别器的图像，虽然亚马逊的工具能检测出最多的人脸，但是谷歌和微软的处理时间明显更快。
![API人脸识别对比](https://images.gitee.com/uploads/images/2019/1129/090532_54bd952d_1648233.png "45f274e2ccc51f17e20be60b73f0076.png")

由于以上API中的使用感和各种使用反馈都达不到我所预期的要求，所以我决定选择一款直接针对人脸检测的API服务平台face++，那么，下面我会从功能的方面对其进行对比，

百度：检测图中的人脸，并为人脸标记出边框。检测出人脸后，可对人脸进行分析，获得眼、口、鼻轮廓等72个关键点定位准确识别多种人脸属性，如性别，年龄，表情（只有笑和不笑）等信息。该技术可适应大角度侧脸，遮挡，模糊，表情变化等各种实际环境

腾讯：对于任意一幅给定的图像，采用智能策略对其进行搜索以确定其中是否含有人脸，如果是则返回人脸的位置、大小和属性分析结果。当前支持的人脸属性有：性别、表情（中性、微笑、大笑）、年龄（误差估计小于5岁）、是否佩戴眼镜（普通眼镜、墨镜）、是否佩戴帽子、是否佩戴口罩。

face++:Face++ Detect API可以检测图片中的人脸，对于检测到的每张人脸，返回其人脸框坐标以及face_token。您可以将face_token传给其他API以进行后续处理和分析。另外，对于最大的5个检测出的人脸，Detect API还可以返回其人脸关键点和人脸属性。

阿里：检测图像中所有人脸的位置和大小，同时定位各人脸器官的位置；支持最多上千个人脸的同时检测，支持平面360度旋转人脸检测，支持左右最大90度侧面人脸检测；可毫秒级完成人脸105个关键点定位。

实际对比：

face++的功能最多，百度其次，阿里和腾讯一般般。
（以上测评内容源于https://blog.csdn.net/where_is_horse/article/details/79826282）

- 总结:经过测评后，我认为face++的人脸识别功能最多，用户体验感相较其他服务平台较佳，返回给用户的数据比较准确与全面，所以我们决定使用face++来完成毕业智能相册的API服务平台。



## 原型

### 原型2：信息设计

#### 产品框架图

![产品架构](https://raw.githubusercontent.com/chanvi-yunqing/API_Graduation-Album/master/%E6%99%BA%E8%83%BD%E7%9B%B8%E5%86%8C%E5%8A%9F%E8%83%BD%E5%9B%BE.jpg)

#### 产品思维导图

![产品思维导图](https://raw.githubusercontent.com/chanvi-yunqing/API_Graduation-Album/master/%E6%99%BA%E8%83%BD%E7%9B%B8%E5%86%8C%E6%80%9D%E7%BB%B4%E5%AF%BC%E5%9B%BE.jpg)







