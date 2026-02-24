# AnyRouter2API

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![GitHub release](https://img.shields.io/github/v/release/IDeLoveYou/anyrouter2api.svg)](https://github.com/IDeLoveYou/anyrouter2api/releases)

> 🚀 **AnyRouter2API** — 将 Cloud Code 客户端内部请求优雅地代理为标准 API 接口，打破平台限制，让任何第三方客户端都能无缝接入和调用！

## 📖 项目简介 (Introduction)

AnyRouter 只支持官方的 Cloud Code 内置客户端。本项目是一个轻量级的请求代理与协议转换工具，它能在本地或服务端拦截并转化 Cloud Code 客户端的通讯协议，将其暴露为一个标准的 HTTP/RESTful 接口（例如兼容 Claude 格式）。

**这意味着什么？**
你可以直接在其他你喜爱的 AI 客户端（如 `LobeHub`、`ChatBox`、`NextChat`）或者任何第三方代码编辑器（如 `Neovim`、`VSCode`、`JetBrains` 侧边栏插件）里，无缝享用 Cloud Code 强大的代码补全和问答能力！

---

## 🚀 快速开始 (Quick Start)

### 方式一：一键部署 (推荐)

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/IDeLoveYou/anyrouter2api)

### 方式二：从源码本地启动
确保你已经安装了所需的环境（如 `Node.js` 和 `uv`）：

```bash
# 1. 克隆项目仓库
git clone https://github.com/IDeLoveYou/anyrouter2api.git
cd anyrouter2api

# 2. 安装依赖包
npm run build

# 3. 启动服务
npm run dev
```
*服务默认将在 `http://127.0.0.1:8787` 运行。*

---

## 🕹️ 如何使用 (Usage)

服务启动后，该代理接口即表现为一个标准的 HTTP API。

接入第三方对话客户端 (如 ChatBox / NextChat)
在第三方客户端的设置（Settings）中，选择 `自定义服务` 或 `Claude 兼容模式`：
- **API URL / 接口地址**: `http://127.0.0.1:8787` (或你的cloudflare workers.dev)
- **API Key / API 密钥**: 任意填写（AnyRouter网站复制的key）
- **Model / 自定义模型名**: 任意填写即可（claude-opus-4-6）

直接保存，即可开始流畅使用你的 Cloud Code 服务！

### 示例

1. LobeHub

2. ChatBox

---

## ⚠️ 免责声明 (Disclaimer)

1. 本项目**仅用于学术研究、技术交流以及个人本地调试**。
2. 开发者不对使用本项目所产生的任何后果负责。请务必遵循相关云服务提供商（Cloud Code 提供方）的**服务条款 (TOS)**。由于高频调用、恶意分享、违规使用而导致账号被封禁或由此引发的其他法律争议，本仓库概不负责。
3. 请合理合规使用，不要用于任何商业用途。

---

## 🙏 鸣谢 (Acknowledgments)

特别感谢 [Darkstarrd-dev/anyrouter-opencode-bridge](https://github.com/Darkstarrd-dev/anyrouter-opencode-bridge) 项目！

本项目在底层接入 AnyRouter (Claude Code API) 时，曾面临严格的 **WAF (Web Application Firewall) 拦截**与 **TLS 指纹校验**问题。通过参考和借鉴该项目中关于伪装请求和处理 TLS 指纹的优秀实现方案。

开源社区的知识共享与互助精神让本项目得以顺利推进，在此对该项目的开发者表示由衷的感谢！

---

## 📄 开源协议 (License)

本项目采用 [MIT License](LICENSE) 协议开源。

---
*If you like this project, please give it a ⭐!*
*Created with ❤️ by [IDeLoveYou](https://github.com/IDeLoveYou)*
```
