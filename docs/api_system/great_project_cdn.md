# 优秀开源项目 CDN 服务

## 简介

镜像优秀开源项目的静态资源以提供高速、可用的内容资源加速服务。

### 特点

---

- 使用腾讯云 CDN 加速
- 提供 7h\*24d 全天候 24 小时不间断服务，如遇服务更新维护会提前 7H 说明
- 中国境内全地可用，延时低于 20ms，且可用性 90 % +（[可用性记录](https://status.gcxstudio.cn)）

---

!> 如果您想使用本服务，请详细阅读文档以便于您更好的进行开发

## 已支持项目

| 项目名                                                  | 项目地址                                             | 版本   | 简介                                                                 |
| ------------------------------------------------------- | ---------------------------------------------------- | ------ | -------------------------------------------------------------------- |
| [Material Design User Interface](https://www.mdui.org/) | [https://www.mdui.org](\https://www.mdui.org/)       | v1.0.2 | MDUI 漂亮、轻量且好用，它能让你更轻松地开发 Material Design 网页应用 |
| [Bootstrap v5](https://getbootstrap.com)                | [https://getbootstrap.com](https://getbootstrap.com) | v5.1.3 | Build fast, responsive sites with Bootstrap                          |

## 调用

按照以下表进行静态资源调用

| 项目名                         | 地址                                                                       | 镜像内容      |
| ------------------------------ | -------------------------------------------------------------------------- | ------------- |
| Material Design User Interface | [https://api.gcxstudio.cn/mdui/](https://api.gcxstudio.cn/mdui/)           | Github 发行版 |
| Bootstrap v5                   | [https://api.gcxstudio.cn/bootstrap/](https://api.gcxstudio.cn/bootstrap/) | 官方资源包    |

## 举例

使用 HTML 调用 MDUI 前端库：

```html
<!-- 调用 MDUI 的 JavaScirpt 资源 -->
<scirpt
  type="text/javascript"
  src="//api.gcxstudio.cn/mdui/js/mdui.min.js"
  crossorigin="anonymous"
></scirpt>
<!-- 调用 MDUI 的 SCSS 文件 -->
<link
  type="text/css"
  rel="stylesheet"
  href="//api.gcxstudio.cn/mdui/css/mdui.min.css"
  crossorigin="anonymous"
/>
```

!> 其他前端库调用方法暂不举例

## 其他

本内容仅发布于 [Gong_cx's Wiki](https://docs.gcxstudio.cn)，禁止盗用内容或转载。

!> 服务器为腾讯云上海，配置有限未启用均衡负载，请勿频繁调用本 API 或进行诸如 CC 攻击等此类无耻的行为

## 技术栈

> 本文档使用 [docsify](https://docsify.js.org/) 构建。
