# 引入

## Gong_cx's API System

您好，欢迎使用 Gong_cx's API System

本 API 具有以下优点以及特点：

---

- 低延时、高可用，24h\*7d 不间断服务
- 提供中国境内 20ms 以内延时的高速体验（[测速记录](http://ping.chinaz.com/api.gcxstudio.cn)）
- 支持 JSON、纯文本等格式进行 Callback
- 提供完整开发文档，完美支持各类开发需求
- 镜像国内优秀前端开源项目

---

仅需要使用 HTTP 进行 GET 请求即可返回信息，

Example（Galgame API）：

```javascript
// 使用 Fetch 获取 API 信息
fetch("//api.gcxstudio.cn/gcxbot_gal/index.php?type=json&name=Gong_cx");
```

返回信息：

```json
// 使用 HTTP 请求将返回以下内容
{
  "API_name": "GALGAME_API",
  "text": "\u7684\u89d2\u8272\u662f\u6bcd\u4eb2\uff0c\u4f60\u7684\u7740\u88c5\u662f\u793e\u957f\uff0c\u4f60\u7ecf\u5386\u7684\u5267\u60c5\u662f\u8272\u8bf1\uff0c\u4f60\u7684\u5916\u8c8c\u7279\u5f81\u662f\u5305\u830e\uff0c\u4f60\u6700\u559c\u6b22\u7684\u9053\u5177\u662f\u97ad\u5b50/\u7ef3\u5b50/\u8721\u70db\uff0c\u4f60\u6700\u559c\u6b22\u7684\u73a9\u6cd5\u662f\u809b\u4ea4\uff0c\u6d17\u8111\u548c\u9732\u51fa",
  "name": "Gong_cx"
}
```

可选各种请求以适配您的服务，便于您的开发，可返回 Unicode 字符或纯文本。

## 当前可提供的服务

如需查看当前可用的 API 服务请查看侧边栏或 [Gong_cx's API System](https://api.gcxstudio.cn) 官网以获取更多关于 API 服务内容的消息。

> Sidebar -> API 服务 -> 您所需的内容

---

## 技术栈

> 本 API 使用通用的脚本型语言 [PHP](https://www.php.net/) 构建，基于 PHP 7.4 版本进行适配。
>
> 本文档使用 [docsify](https://docsify.js.org/) 构建。
