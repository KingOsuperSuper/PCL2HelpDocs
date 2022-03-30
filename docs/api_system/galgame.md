# Galgame 人设 API

## 简介

趣味的 Galgame 人设随机生成服务，提供 210 条重复的随机内容。

### 特点

---

- 提供多达 210 条随机人设文案
- 可返回 JSON 或 纯文本内容以方便调用
- 中国境内全地可用，且可用性 90 % +（[可用性记录](https://status.gcxstudio.cn)）

---

!> 如果您想使用本服务，请详细阅读文档以便于您更好的进行开发

## 调用

您可以使用任何支持解析 JSON 字符组和发起 HTTP 请求的编程语言调用本服务。

本 API 服务的请求地址为：[https://api.gcxstudio.cn/gcxbot_gal/index.php](https://api.gcxstudio.cn/gcxbot_gal/index.php)

### 可使用参数

| 请求名    | 可用参数                                                                                                                        | 必填 | 简介                           |
| --------- | ------------------------------------------------------------------------------------------------------------------------------- | ---- | ------------------------------ |
| name      | 类型：str 可使用 UTF-8 请求该参数                                                                                               | 是   | 可自定义用于返回人设的作用人名 |
| type      | 类型：str 可选择使用 json, json_text 和 text                                                                                    | 否   | 用于自定义 API 返回类型        |
| type 详解 | 使用 json 类型时，将会返回请求的 name 和随机人设，使用 json_text 时，将会返回组合后的人设，使用 text 时，将会返回组合后的纯文本 | 否   | type 请求详解                  |

## 举例

使用 PHP 调用：

```php
try {
    ini_set('default_socket_timeout', 1);
    $motd = file_get_contents("https://api.gcxstudio.cn/gcxbot_gal/index.php?name=xxx&type=json_text");
}
```

使用此方法将会携带自定义内容尝试请求 Galgame 人设 API，并返回以下内容 ：

```json
{
  "text": "xxx的角色是拟人化，你的着装是和服，你经历的剧情是日常/生活，你的外貌特征是阴毛/腋毛，你最喜欢的道具是眼镜，你最喜欢的玩法是轮奸，颜射和潮吹"
}
```

此时可通过

```php
$galgame = json_decode($motd);
echo($galgame->text);
```

显示 JSON 文件中的 text 数据。

!> 其他编程语言示例暂不提供。

## 其他

本内容仅发布于 [Gong_cx's Wiki](https://docs.gcxstudio.cn)，禁止盗用内容或转载。

!> 服务器为腾讯云上海，配置有限未启用均衡负载，请勿频繁调用本 API 或进行诸如 CC 攻击等此类无耻的行为

## 技术栈

> 本 API 使用通用的脚本型语言 [PHP](https://www.php.net/) 构建，基于 PHP 7.4 版本进行适配。
>
> 本文档使用 [docsify](https://docsify.js.org/) 构建。
