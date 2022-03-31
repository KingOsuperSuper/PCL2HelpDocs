# Bing 每日一图 API

## 简介

完善的 Bing 每日一图 API，快速且有效的获取每日一图，经过 CDN 加速后任播至中国全部地区

### 特点

---

- 使用腾讯云 CDN 加速
- 可返回 JSON、XML 及图片形式以方便调用
- 中国境内全地可用，且可用性 90 % +（[可用性记录](https://status.gcxstudio.cn)）

---

!> 如果您想使用本服务，请详细阅读文档以便于您更好的进行开发

## 调用

您可以随意所有支持直接展示远程外链图片的程序或支持解析 JSON 或 XML 的编程语言

本 API 服务的请求地址为：[https://api.gcxstudio.cn/bing.php](https://api.gcxstudio.cn/bing.php)

### 可使用参数

| 请求名    | 可用参数                                                                                                                                                 | 必填   | 简介                    |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ----------------------- |
| type      | 类型：str 可选择使用 json, xml 和 image                                                                                                                  | 是     | 用于自定义 API 返回类型 |
| type 详解 | 使用 json 类型时，将会返回官方提供的 JSON 数据镜像，使用 xml 时，将会返回 XML 格式的信息，使用 image 时，将会返回解析后的图片（MIME Type 为 image/jpeg） | Unknow | type 请求详解           |

## 举例

使用 PHP 调用：

```php
try {
    ini_set('default_socket_timeout', 1);
    $motd = file_get_contents("https://api.gcxstudio.cn/bing.php?type=json");
}
```

使用此方法将会携带自定义内容尝试请求 Bing 每日一图 API，并返回以下内容 ：

```json
{
  "images": [
    {
      "startdate": "20220331",
      "fullstartdate": "202203311600",
      "enddate": "20220401",
      "url": "/th?id=OHR.HawaMahalJaipur_ZH-CN3863273823_1920x1080.jpg&rf=LaDigue_1920x1080.jpg&pid=hp",
      "urlbase": "/th?id=OHR.HawaMahalJaipur_ZH-CN3863273823",
      "copyright": "哈瓦泰姬陵，印度拉贾斯坦邦，斋浦尔市 (© Mazur Travel/Shutterstock)",
      "copyrightlink": "https://www.bing.com/search?q=%E5%9F%83%E5%8F%8A&form=hpcapt&mkt=zh-cn",
      "title": "朝向世界的皇家窗口",
      "quiz": "/search?q=Bing+homepage+quiz&filters=WQOskey:%22HPQuiz_20220331_HawaMahalJaipur%22&FORM=HPQUIZ",
      "wp": true,
      "hsh": "ba0298793885de6cb666364cfc8b7303",
      "drk": 1,
      "top": 1,
      "bot": 1,
      "hs": []
    }
  ],
  "tooltips": {
    "loading": "正在加载...",
    "previous": "上一个图像",
    "next": "下一个图像",
    "walle": "此图片不能下载用作壁纸。",
    "walls": "下载今日美图。仅限用作桌面壁纸。"
  }
}
```

此时可通过

```php
$image_str = json_decode($motd);
$imgurl = 'http://cn.bing.com'.$image_str['images'][0]['url'];
echo($imgurl)
```

显示 JSON 文件中 images 组下的 url 的数据。

!> 其他编程语言示例暂不提供。

## 其他

本内容仅发布于 [Gong_cx's Wiki](https://docs.gcxstudio.cn)，禁止盗用内容或转载。

!> 服务器为腾讯云上海，配置有限未启用均衡负载，请勿频繁调用本 API 或进行诸如 CC 攻击等此类无耻的行为

## 技术栈

> 本 API 使用通用的脚本型语言 [PHP](https://www.php.net/) 构建，基于 PHP 7.4 版本进行适配。
>
> 本文档使用 [docsify](https://docsify.js.org/) 构建。
