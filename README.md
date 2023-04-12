APISpace 介绍

**本** **API** **服务由** **[APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=aigc)** **提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。

APISpace 提供15种开发语言的代码示例，分别是：

-   Java(OK HTTP)
-   HTTP
-   cURL
-   微信小程序
-   PHP(pecl_http)、PHP(cURL)
-   Python(http.client)、Python(Requests)
-   JavaScript(Jquery AJAX)、JavaScript(XHR)
-   NodeJS(Native)、NodeJS(Request)
-   Ruby(Net:Http)
-   Shell(Httpie)、Shell(cUrl)

  


# **AI** **绘画**

【AI绘画/AI作画/AI画画/AI图像生成】开箱即用，轻松将先进的图文 AI 融入您的产品。该API提供稳定的服务，满足各行业、各场景、不同用量的 AI 创作需求。

**使用该产品前，您需要通过** **[https://www.apispace.com/23329/api/aigc/introduction](https://www.apispace.com/23329/api/aigc/introduction?utm_source=github&utm_term=aigc)** **申请** **API** **服务。**

本文档末尾提供了 Python(Requests) 的调用代码示例，可以前往文档末尾查看。

更多代码示例：[https://www.apispace.com/23329/api/aigc/guidence/](https://www.apispace.com/23329/api/aigc/guidence/?utm_source=github&utm_term=aigc)

**该产品拥有以下APIs：**

1.  AI 绘画文生图 API
1.  AI 绘画图生图 API
1.  人像照片转动漫 API
1.  AI 图片高清(超高分辨率) API

  


### **API** **列表**

**1.** **AI** **绘画文生图**

-   **接口说明：** 输入文本描述，生成符合文本描述的图像，可用于 AI 绘画等场景。调用接口 1 次生成 1 张图片，接口中包含违规图片检测（涉⻩、涉政、涉暴、敏感信息）。
-   **示意图：**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/26c94f13a08248a3a1a41f8e6f62a257~tplv-k3u1fbpfcp-zoom-1.image)

**2.** **AI** **绘画图生图**

-   **接口说明：** 输入图片和文本描述，生成符合图片参考和文本描述的图像，可用于 AI 绘画等场景。调用接口 1 次生成 1 张图片，接口中包含违规图片检测（涉⻩、涉政、涉暴、敏感信息）。
-   **示意图：**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/112466472dfb4bc5bcdc6d1be664689d~tplv-k3u1fbpfcp-zoom-1.image)

**3. 人像照片转动漫**

-   **接口说明：** 输入人像照片及风格选项，生成该风格的该人像艺术风格化图像。直接用预置的风格和人像照片 URL 生成对应的动漫风格图片，而不需要指定提示词（prompt）。
-   **示意图：**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e1895263d84642d082d8d11ff25f2be8~tplv-k3u1fbpfcp-zoom-1.image)

**4.** **AI** **图片高清(超高分辨率)**

-   **接口说明：** 输入文本描述，生成符合文本描述的图像，可用于 AI 绘画等场景。对目标图填充细节并输出高清图（宽、高各提升 4 倍，总计提升 16 倍分辨率）。例如：512 × 512 的图片高清后输出 2048 × 2048 的图。
-   **示意图：**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/315c27e3d3e24a8e8014c2f9f9738134~tplv-k3u1fbpfcp-zoom-1.image)

  


### **使用须知**

1.  由于敏感图等问题提交任务成功但生成失败的，将退还次数。
1.  一般标准分辨率为 512×512，生成图片宽、高最多支持 768×768；如需更高清的图片，建议使用**图像高清化**功能进行高清处理。
1.  输入内容可以是中文或英文，本接口会自动屏蔽掉敏感的提示词。
1.  生成一张512 × 512的图，约耗时6~8s（不算排队和网络传输）；**生成结束后将通过回调地址返回结果**。
1.  对 512 × 512 的图片高清化，约耗时3~6s（不算排队和网络传输）；**生成结束后将通过回调地址返回结果**。

### **精选** **AI** **绘画作品与关键词（Prompt）**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ad81e09da495435ab2866f523ba6e0a7~tplv-k3u1fbpfcp-zoom-1.image)

> **Prompt：** 高品质3d渲染，超现实主义非常可爱，柔和的色彩蓬松！皮卡丘混血猫，高度细致，vray 平滑，侦探皮卡丘风格，hannah yata charlie immer，柔和的室内光线，低角度，uhd 8 k，清晰对焦，高清

  


![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/bf1d728cc2e449578b7f68e032273a5a~tplv-k3u1fbpfcp-zoom-1.image)

> **Prompt：** 穿着华丽纹路复杂的银饰铠甲，拟人化的兔子，对称，灵性的眼睛，史诗感美丽，华丽，超细节，超清晰，电影级滤镜，16k，徕卡50mm定焦镜头

  


![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/148deaaa2d1f40c7adee3dcf38545033~tplv-k3u1fbpfcp-zoom-1.image)

> **Prompt：** 令人惊叹的河边小屋，artstation冠军，Victo Ngai、Kilian Eng 和 Jake Parker的艺术品，充满活力的漩涡色彩线，获奖杰作，极其艳丽，美学，辛烷值渲染，8K 高清分辨率，高度详细

  


![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9fe5e5c0d091485396dde476c43135cc~tplv-k3u1fbpfcp-zoom-1.image)

> **Prompt：** 完整而精致的白色九尾狐肖像，美丽，高贵，敏捷，仙女，神话，传说，详细，artstation上的趋势，灯光效果，kilian eng，john harris，bastien lecouffe - deharme的，高度详细

  


![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9186d8503f8647e5b82aa0e79a511590~tplv-k3u1fbpfcp-zoom-1.image)

> **Prompt：** 白色，云中的梦幻城堡，次表面散射，鲜艳的色彩，（（（锦鲤颜色））），辛烷值渲染，jesper ejsing，james jean，justin gerard，tomasz alen kopera，cgsociety，fenghua zhong，makoto shinkai，非常详细，边缘光, 艺术, 电影照明, 非常连贯, 超现实主义, 高细节, 8 k , 壁纸

  


![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/44b83d4a292d41648a56eff279ca4e54~tplv-k3u1fbpfcp-zoom-1.image)

> **Prompt：** 非常详细的威尼斯洛可可画，描绘了一个郁郁葱葱的花园，满是柔和的粉红玫瑰，没有人，地平线上的金色城堡，蓝色蝴蝶，柔和的华丽背景，体积照明，花卉，幻想，逼真，数字插图，krenz cushart 的艺术，alphonse mucha, kehinde wiley, artem demura , 8k, 高清

  


![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/5934888259b24a0b9f4578c7785bdf03~tplv-k3u1fbpfcp-zoom-1.image)

> -   **Prompt：** 大地之母，高度详细，数字绘画，艺术站，概念艺术，流畅，清晰的焦点，插图，电影照明，artgerm 和 greg rutkowski 和 alphonse Mucha 的艺术，高清

  


### **关键词（Prompt）知识**

想要生成绝美的画作，用好关键词（Prompt）很重要！！！点击下方，让你快速掌握关键词（Prompt）技巧！

👉👉👉：[关键词（Prompt 知识）](https://easy-open-link.feishu.cn/wiki/wikcnmylZReDlk6kENwMvsMAgce)

  


### **回调地址返回参数示例**

```
{
    “uid”: “b50fd9dc699b0f69e5dac9d150939c94”, //任务ID
    “success”: True, // 1、True成功 2、False失败
    “data”: {
        “uid”: “b50fd9dc699b0f69e5dac9d150939c94”, // 任务ID
        “cdn”: “https://ailab-huawei-cdn.nolibox.com/aigc/images/d6fa33b93ac84b8fbb233f4be03ba38f.png“, // 加速图片地址。safe为False时，该字段返回空字符串
        “cos”: “https://ailab-1d01.obs.cn-north-4.myhuaweicloud.com/aigc/images/d6fa33b93ac84b8fbb233f4be03ba38f.png“, // 图片地址。safe为False时，该字段返回空字符串
        “safe”: True, // 图片是否安全。success为True时也会返回False
        “reason”: “”, // 错误原因
        “createtime”: 1680079480.1837924, // 提交任务执行时间
 “starttime”: 1680079480.189582, // 任务执行开始时间
 “end_time”: 1680079483.7931507, // 任务执行结束时间
 “duration”: 3.609358310699463, // 执行任务持续时间
 “elapsed_times”: { // 此参数不需要关注，为任务执行耗时时间
 “pending”: 0.005789756774902344, 
 “run_algorithm”: 3.001178503036499, 
 “algorithm_latencies”: { 
 “get_model”: 0.5092508792877197, 
 “inference”: 2.4906301498413086, 
 “cleanup”: 0.000007867813110351562, 
 “__total“: 2.9998888969421387
            },
            “upload”: 0.3074338436126709,
            “audit”: 0.29493021965026855
        },
        “request”: { // 请求的入参
            “task”: “txt2img.sd”,
            “model”: {
                “callback_url”: “”,
                “use_circular”: “”,
                “seed”: -1,
                “variation_seed”: 0,
                “variation_strength”: 0,
                “variations”: [],
                “num_steps”: 20,
                “guidance_scale”: 7.5,
                “negative_prompt”: “”,
                “is_anime”: “”,
                “version”: “dreamlike_v1”,
                “sampler”: “k_euler”,
                “clip_skip”: -1,
                “custom_embeddings”: {},
                “max_wh”: 1024,
                “text”: “Roses”,
                “w”: 512,
                “h”: 512
            }
        }
    }
}
```

  


### **服务保障**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a9e90ca20a4841e9b98b525389762517~tplv-k3u1fbpfcp-zoom-1.image)

  


### **Python(Requests) 调用代码示例**

这里以 AI 绘画文生图 API 为例

```
import requests

url = "https://23329.o.apispace.com/aigc/txt2img"

payload = {"task":"txt2img.sd","params":{"model":"art","text":"玫瑰花","w":512,"h":512,"guidance_scale":7.5,"negative_prompt":"cropped","sampler":"k_euler","seed":-1,"num_steps":20},"model":"art","text":"玫瑰花","w":512,"h":512,"guidance_scale":7.5,"negative_prompt":"cropped","sampler":"k_euler","seed":-1,"num_steps":20,"notify_url":""}

headers = {
    "X-APISpace-Token":"",
    "Authorization-Type":"apikey",
    "Content-Type":"application/json"
}

response=requests.request("POST", url, data=json.dumps(payload), headers=headers)

print(response.text)

```
