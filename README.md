# Summora - AI 浏览器侧边栏助手

<p align="center">
  <img src="assets/logo.png" width="128" height="128" alt="Summora Logo">
</p>

<p align="center">
  <strong>开源的浏览器侧边栏 AI 助手</strong>
</p>

<p align="center">
  <a href="#功能特性">功能</a> •
  <a href="#安装">安装</a> •
  <a href="#使用方法">使用</a> •
  <a href="#隐私说明">隐私</a> •
  <a href="#chrome-web-store-上架信息">上架</a>
</p>

---

## 简介

Summora 是一个开源的浏览器扩展，在您的浏览器中提供一个 AI 侧边栏助手，帮助您：

- 一键总结网页内容
- 提取视频（YouTube、Bilibili）标题和字幕进行总结
- 在搜索引擎结果页获得 AI 生成的摘要
- 基于当前页面内容与 AI 对话

**核心优势**：隐私优先设计，您完全掌控自己的数据和 API 配置。

---

## 功能特性

### 📝 网页总结
- 一键提取当前页面内容（最多 5000 字符）
- 智能生成关键要点和简短摘要
- 支持多种内容类型的个性化提示

### 🎬 视频支持
- **YouTube**：提取标题、描述和自动字幕
- **Bilibili**：提取标题和描述信息
- 针对视频内容优化的总结提示

### 🔍 搜索增强
- 支持 Google、Bing、百度等主流搜索引擎
- 在搜索结果页注入 AI 摘要卡片
- **需要用户明确授权**，保护搜索隐私

### 💬 智能对话
- 基于当前页面上下文的 AI 对话
- 自动检测浏览器语言并响应（支持 28+ 语言）
- Markdown 格式渲染

### ⚙️ 自定义模型
- 支持任何 OpenAI 兼容的 API
- 可配置多个模型并切换
- 支持 OpenAI、Azure OpenAI、DeepSeek、本地 LLM 等

### 🎨 灵活界面
- 可调整宽度的侧边栏（280-600px）
- 可收起为浮动按钮
- 不影响网页正常使用

---

## 安装

### 从 Chrome Web Store 安装（推荐）

_即将上架，敬请期待..._

### 开发者模式安装

1. 克隆仓库
```bash
git clone https://github.com/JackDance/summora.git
cd summora
```

2. 安装依赖
```bash
pnpm install
```

3. 开发模式
```bash
pnpm dev
```

4. 生产构建
```bash
pnpm build
```

5. 加载到 Chrome
   - 打开 `chrome://extensions/`
   - 开启"开发者模式"
   - 点击"加载已解压的扩展程序"
   - 选择 `build/chrome-mv3-prod` 目录

---

## 使用方法

### 首次使用

1. 点击浏览器工具栏的 Summora 图标，或按快捷键打开侧边栏
2. 点击右上角的设置按钮（⚙️）
3. 添加您的 AI 模型配置：
   - **名称**：给模型起个名字（如"我的 GPT-4"）
   - **API 端点**：如 `https://api.openai.com/v1`
   - **模型 ID**：如 `gpt-4`、`gpt-3.5-turbo`
   - **API Key**：您的 API 密钥
4. 保存并选择该模型为默认模型

### 总结网页

1. 打开任意网页
2. 点击 Summora 图标打开侧边栏
3. 点击"总结"按钮
4. 等待 AI 生成总结

### 搜索增强

1. 在 Google、Bing 或百度搜索任意关键词
2. 页面顶部会出现授权询问卡片
3. 点击"启用"授权后，即可看到 AI 生成的搜索摘要

### 对话功能

直接在侧边栏底部的输入框输入问题，AI 会基于当前页面内容回答。

---

## 隐私说明

### 🔒 数据保护承诺

| 我们存储的 | 我们不存储的 |
|-----------|-------------|
| 您的模型配置（本地加密） | 浏览历史 |
| 侧边栏偏好设置 | 网页内容 |
| 搜索授权偏好 | 聊天记录 |

### 📡 数据传输

- **AI 服务通信**：网页内容和对话仅发送到**您自己配置的 API 端点**
- **无中间服务器**：我们不会将您的数据发送到任何第三方服务器
- **安全建议**：建议配置 HTTPS 端点以确保传输加密

### 🔐 权限使用

| 权限 | 用途 | 必要性 |
|------|------|--------|
| `activeTab` | 获取当前标签页信息，发送消息 | 必需 |
| `storage` | 存储配置和偏好（本地） | 必需 |
| `scripting` | 动态注入内容脚本 | 必需 |
| `<all_urls>` | 在所有网站显示侧边栏 | 必需 |

### 🚫 我们不会

- ❌ 追踪您的浏览历史
- ❌ 出售或共享您的数据
- ❌ 使用 Google Analytics 或遥测
- ❌ 执行远程代码
- ❌ 收集用户身份信息

### 📄 完整隐私政策

查看 [PRIVACY.md](./PRIVACY.md) 了解完整隐私政策。

---

## Chrome Web Store 上架信息

### 单一用途说明

本扩展的唯一目的是：在浏览器中提供一个 AI 侧边栏助手，帮助用户总结网页和视频内容，并在搜索页面提供 AI 生成的摘要。

### 合规说明

- ✅ 使用 Manifest V3 标准
- ✅ 提供详细隐私政策
- ✅ 用户明确控制功能启用
- ✅ 所有数据本地存储
- ✅ 无遥测或跟踪代码

### 商店描述

完整的上架材料请查看 [STORE_LISTING.md](./STORE_LISTING.md)

---

## 技术栈

- [Plasmo Framework](https://www.plasmo.com/) - 浏览器扩展框架
- [React 18](https://react.dev/) - UI 框架
- [TypeScript](https://www.typescriptlang.org/) - 类型安全
- Manifest V3 - Chrome 扩展标准

---

## 开发

### 开发服务器

```bash
pnpm dev
```

### 构建生产版本

```bash
pnpm build
```

### 打包分发

```bash
pnpm package
```

---

## 贡献

欢迎提交 Issue 和 Pull Request！

### 开发规范

- 使用 TypeScript 编写代码
- 遵循现有代码风格
- 提交前运行测试

---

## 许可证

[MIT License](./LICENSE)

---

<p align="center">
  使用 ❤️ 和 🔒 隐私保护理念构建
</p>
