# Jmcomic-Local

本地部署的 JMComic3（禁漫）Web 客户端。

通过静态文件本地托管，前端直接调用官方 API 访问禁漫内容。只需联网即可使用，无需后端服务器。

## 项目简介

本项目是 JMComic3 的静态 Web 版本，包含完整的前端资源（HTML、CSS、JS、图标、Service Worker 等）。

- **纯静态部署**：下载后用任意支持静态文件的平台即可运行
- **官方 API**：直接请求禁漫官方接口，保持功能同步
- **本地优先**：所有页面和资源本地加载，仅数据请求走网络
- **PWA 支持**：可安装为桌面/手机应用，支持离线缓存页面

## 功能特点

- 浏览、搜索、分类、排行榜
- 在线阅读漫画
- 收藏、历史记录等个人功能（需登录）
- 响应式设计，适配电脑与手机
- Service Worker 支持离线访问静态资源

## 下载

请前往 **[Releases（发行版）](https://github.com/shuo156/Jmcomic-Local/releases)** 下载最新版本的压缩包。

不建议直接 clone 源码，推荐使用发行版打包好的文件。

## 快速开始

### 1. 部署到静态托管平台

本项目为纯静态资源，可部署到任何支持静态文件的地方，例如：

- **Cloudflare Pages**（推荐）
- GitHub Pages
- Vercel
- Netlify
- 本地服务器（Python / Node.js / Nginx 等）

以 **Cloudflare Pages** 为例：

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 进入 **Workers & Pages** → **Create application** → **Pages**
3. 上传发行版解压后的文件夹，或连接本仓库
4. 构建配置可留空（纯静态，无需构建）
5. 部署完成后获得访问地址

### 2. 本地快速预览（可选）

```bash
# Python 3
python -m http.server 8080

# 或使用 Node.js
npx serve -p 8080