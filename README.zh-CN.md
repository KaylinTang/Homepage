<div align="center">

# 个人作品集主页

一个用于展示项目、经历、研究成果与技术能力的轻量、响应式、无障碍友好个人主页。

[English README](README.md) · [在线访问](https://kaylintang.github.io/Homepage-luka-template/)

</div>

> [!NOTE]
> 本站基于 [Yuheng Yang](https://wzsyyh.github.io/) 的 [Luka Homepage Template](https://github.com/wzsyyh/luka-homepage-template) 改造。感谢原作者提供温暖、简洁的设计基础。

## 项目简介

这个仓库是个人作品集主页的源代码，内容重点涵盖云基础设施、软件开发、数据与应用计算。网站沿用清晰的学术主页结构，将个人简介、项目、经历和研究成果整理为便于浏览的单页作品集；实现上保持克制，仅使用静态 HTML、CSS 与原生 JavaScript。

为保护隐私，本文档不重复公开联系方式、个人文件或其他敏感信息。对外展示的个人资料由网站页面统一维护。

## 主要栏目

| 栏目 | 展示内容 |
| --- | --- |
| About | 简要的专业背景与关注方向 |
| Education | 以时间线呈现教育经历 |
| Projects | 精选全栈、云、数据与 Web 项目，以及技术栈和成果 |
| Experience | 实习、技术、分析与行业经历 |
| Research | 论文发表与航空碳排放研究经历 |
| Skills | 云平台、软件开发、系统、数据库、工程流程与语言能力 |
| Awards | 精选学术荣誉 |

## 核心特性

- 响应式布局：桌面端采用固定侧栏与内容双栏，平板和手机端自动切换为单栏。
- 明暗主题：自动读取系统偏好，并通过本地存储保留访客选择。
- 页面导航：固定顶部导航、平滑锚点跳转与返回顶部入口。
- 时间线展示：统一组织教育、项目、工作与研究内容。
- 邮箱复制交互：使用 Clipboard API，并为旧浏览器提供后备方案和无障碍状态提示。
- 轻量入场动画：通过 `IntersectionObserver` 按需触发内容显示。
- 无障碍细节：支持减少动态效果、键盘焦点、语义化区块和描述性 ARIA 标签。
- 搜索与分享优化：包含 SEO、Open Graph 及 X/Twitter Card 元数据。
- 零构建：不依赖前端框架、包管理器、数据库或编译流程。

## 技术方案

| 层级 | 技术 |
| --- | --- |
| 页面结构 | HTML5 |
| 样式 | CSS3、自定义属性、响应式媒体查询 |
| 页面交互 | 原生 JavaScript、Clipboard API、`localStorage`、`matchMedia`、`IntersectionObserver` |
| 字体与图标 | Google Fonts、Font Awesome、Academicons |
| 托管与自动化 | GitHub Pages、GitHub Actions |

## 目录结构

```text
.
├── .github/workflows/static.yml  # GitHub Pages 部署工作流
├── assets
│   ├── css                       # 字体与主题样式
│   ├── cv                        # 本地管理的文档资源
│   ├── img                       # 头像、项目与机构图片
│   └── js                        # 小型兼容性脚本
├── index.html                    # 页面内容、元数据与交互逻辑
├── README.md
├── README.zh-CN.md
├── RELEASE_NOTES.md
└── LICENSE.md
```

## 本地运行

项目完全由静态文件组成，可以直接用浏览器打开。建议启动本地 HTTP 服务，使浏览器 API 和相对资源路径的行为与线上环境保持一致：

```bash
python3 -m http.server 8000
```

随后访问 `http://localhost:8000`。无需安装依赖或执行编译。

## 部署方式

网站通过 `.github/workflows/static.yml` 中的工作流自动部署静态内容：

1. 推送到 `main` 分支，或在 Actions 页面手动触发工作流。
2. GitHub Actions 检出仓库并配置 GitHub Pages。
3. 整个仓库被打包为 Pages artifact。
4. GitHub Pages 将该 artifact 发布到生产环境。

如需部署 fork，请在仓库设置中启用 **GitHub Pages**，并选择 **GitHub Actions** 作为发布来源。同时应将 `index.html` 中的 canonical URL 和社交分享 URL 更新为新域名。

## 内容维护

- 在 `index.html` 中更新页面文案和各栏目条目。
- 在 `assets/css/theme-luka.css` 中调整颜色变量、间距、字体、布局和响应式断点。
- 替换 `assets/img/` 中的图片时，为图片保留准确、有意义的替代文本。
- 除非确定需要公开，否则不要将个人文件或联系方式提交到版本控制。
- 站点域名变更后，应同步更新 canonical、Open Graph 与 X/Twitter 元数据。

## 隐私说明

本文档不会重复联系方式、私人文件或不必要的个人信息。公开 fork 前，请再次检查 HTML 与静态资源，确认其中不包含不应公开的元数据或文件。

## 许可证

本仓库适用的许可条款请参阅 [LICENSE.md](LICENSE.md)。
