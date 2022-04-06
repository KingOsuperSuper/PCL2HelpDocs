# 优秀开源项目 CDN 服务

## 简介

镜像优秀开源项目的静态资源以提供高速、可用的 CDN 任播服务

### 特点

---

- 使用腾讯云 CDN 加速
- 提供 7h\*24d 全天候 24 小时不间断服务，如遇服务更新维护会提前 7H 说明
- 中国境内全地可用，延时低于 20ms，且可用性 90 % +（[可用性记录](https://status.gcxstudio.cn)）

---

!> 如果您想使用本服务，请详细阅读文档以便于您更好的进行开发

## 已支持项目

!> 为节省流量及性能开销，除必须标明版本号的项目，均只镜像最新版本以及主流版本

| 项目名                                                    | 项目地址                                             | 版本    | 简介                                                                 |
| --------------------------------------------------------- | ---------------------------------------------------- | ------- | -------------------------------------------------------------------- |
| [Material Design User Interface](https://www.mdui.org/)   | [https://www.mdui.org](\https://www.mdui.org/)       | v1.0.2  | MDUI 漂亮、轻量且好用，它能让你更轻松地开发 Material Design 网页应用 |
| [Bootstrap v5](https://getbootstrap.com)                  | [https://getbootstrap.com](https://getbootstrap.com) | v5.1.3  | Build fast, responsive sites with Bootstrap                          |
| [Argon Theme](https://github.com/solstice23/argon-theme/) | https://github.com/solstice23/argon-theme/           | v1.3.5  | Argon - 一个轻盈、简洁、美观的 WordPress 主题                        |
| [jQuery](https://jquery.com)                              | [https://jquery.com](https://jquery.com)             | v3.6.0  | Fast, small, and feature-rich JavaScript library.                    |
| [Docsify ](https://docsify.js.org)                        | [https://docsify.js.org](https://docsify.js.org)     | v4.12.2 | A magical documentation generator.                                   |
| [Font Awesome Free](https://fontawesome.com)              | [https://fontawesome.com](https://fontawesome.com)   | v6.1.1  | Take the hassle out of icons in your website.                        |

## 调用

按照以下表进行静态资源调用

| 项目名                         | 地址                                                                               | 资源路径          | 镜像内容      |
| ------------------------------ | ---------------------------------------------------------------------------------- | ----------------- | ------------- |
| Material Design User Interface | [https://api.gcxstudio.cn/mdui/](https://api.gcxstudio.cn/mdui/)                   | Github 发行版路径 | Github 发行版 |
| Bootstrap v5                   | [https://api.gcxstudio.cn/bootstrap/](https://api.gcxstudio.cn/bootstrap/)         | 官方资源包路径    | 官方资源包    |
| Argon Theme                    | [https://api.gcxstudio.cn/argon/v%theme_version%](https://api.gcxstudio.cn/argon/) | Github 发行版路径 | Github 发行版 |
| jQuery                         | [https://api.gcxstudio.cn/jquery/version](https://api.gcxstudio.cn/jquery/)        | jsDelivr 路径     | 官方资源包    |
| Docsify & 官方插件             | [https://api.gcxstudio.cn/docsify ](https://api.gcxstudio.cn/docsify)              | jsDelivr 路径     | Github 发行版 |
| Font Awesome Free              | [https://api.gcxstudio.cn/font-awesome](https://api.gcxstudio.cn/font-awesome)    | 官方资源包路径    | 官方资源包    |

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
