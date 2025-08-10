# Open-GPT

<div align="center">
  <h3>🤖 一个现代化的 AI 聊天应用</h3>
  <p>基于 Electron 构建的跨平台 AI 聊天客户端，支持多种 AI 模型</p>

  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="license"/>
  <img src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey.svg" alt="platform"/>
  <img src="https://img.shields.io/badge/Electron-27.0.0-47848f.svg" alt="electron"/>
  <img src="https://img.shields.io/badge/Vue.js-3.3.11-4fc08d.svg" alt="vue"/>
  <img src="https://img.shields.io/badge/version-v1.0.1-brightgreen" alt="version"/>
</div>


> 单文件即用版：本仓库以 `Open-Chat.html` 为主页面，已提供 Electron 打包配置，可一键打包为 Windows 安装包。

![screenshot](./%E4%B8%8B%E8%BD%BD%20(4).png)

---

## ✨ 功能特性

- 🎯 多模型支持：OpenAI、OpenRouter、以及自定义 API 提供商
- 💬 智能对话：支持流式与非流式响应，Markdown 渲染与代码高亮
- 📱 响应式设计：桌面与移动端皆有良好体验
- 🔧 自定义配置：API URL、API Key、系统提示词、自定义模型管理
- 📚 历史记录：本地保存与加载对话历史，支持快速切换会话
- 🎨 现代 UI：Tailwind CSS + 动效完善的交互体验
- ⚡ 强化交互：发送按钮脉冲、悬停、点击反馈、水波纹、加载与成功反馈动画

---

## 🚀 下载与快速开始

### 方式一：下载安装包（推荐）
1. 前往 [Releases](../../releases) 下载最新版本
2. 下载 `Open-GPT Setup 1.0.1.exe`（Windows）
3. 运行安装程序并完成安装
4. 启动应用后在“设置”中配置 API 提供商与密钥

### 方式二：从源码运行
```bash
# 克隆仓库（或将当前文件夹作为项目根目录）
# git clone https://github.com/your/repo.git
# cd open-gpt

# 安装依赖
npm install

# 启动开发（Electron）
npm start

# 构建打包（安装包输出在 dist/）
npm run dist
```

> 也可直接双击 `Open-Chat.html` 在浏览器中打开；或使用本地静态服务器：`python -m http.server 8000` 后访问 `http://localhost:8000/Open-Chat.html`。

---

## ⚙️ 配置说明

1. 点击右上角“设置”图标打开设置面板
2. 选择 API 提供商：
   - OpenAI：使用官方 OpenAI API
   - OpenRouter：聚合服务，提供多家模型
   - 自定义：可配置自有 API 端点
3. 输入对应的 API Key
4. 选择或添加模型（支持自定义模型 ID 与显示名称）
5. 可选：编辑系统提示词（System Prompt）

### 支持的模型
- OpenAI：支持最新模型，自动获取并显示可用列表，支持排序与优先级标记
- OpenRouter：覆盖 100+ 开源/商业模型，区分免费与付费并显示定价信息

---

## 🛠️ 技术栈
- 前端：Vue.js（CDN 引入）、Tailwind CSS、Font Awesome、Marked.js
- 桌面端：Electron 27
- 构建：electron-builder（NSIS 安装包）

---

## 📁 项目结构
```
Open-Chat/
├── Open-Chat.html           # 主页面（模板/样式/逻辑与动效）
├── main.js                  # Electron 主进程入口
├── package.json             # 项目与打包配置
├── README.md                # 项目说明（本文件）
├── dist/                    # 构建输出目录
│   ├── Open-GPT Setup 1.0.1.exe        # Windows 安装包
│   └── win-unpacked/                    # 未打包应用文件
└── 下载 (4).png              # 截图示例
```

---

## 🎯 使用指南
- 基本对话：在底部输入框输入问题（占位提示：`Ask anything`），按 Enter 或点击发送
- 历史记录：左侧侧边栏查看/切换历史会话
- 新建对话：顶部“+”按钮即可
- 欢迎标题：`I'm Open-GPT  How can I help?`
- 模型展示：`Model：<当前选择模型>`

---

## 📝 更新日志

### v1.0.1
- 新增
  - 发送按钮交互增强：脉冲动画、点击反馈、悬停缩放/阴影/颜色过渡、图标弹跳、加载态动画、水波纹与成功反馈
  - 新增方法：`handleSendButtonClick`、`addRippleEffect`；新增数据状态：`buttonClickEffect`
  - 引入 Electron 配置与打包脚本，支持一键构建 Windows 安装包
- 修改
  - 欢迎标题改为：`I'm Open-GPT  How can I help?`
  - 模型标签从“当前模型：”改为“Model：”
  - 输入框占位提示从“问我任何问题”改为 `Ask anything`
- 输出
  - 生成安装包：`dist/Open-GPT Setup 1.0.1.exe`

### v1.0.0（2024-01-09）
- 初始版本发布
- 支持多种 AI 模型
- 实现流式对话
- 响应式界面设计
- 完整的配置系统

---

## ❓ 常见问题（FAQ）
- 控制台出现 `404 /@vite/client`：使用静态服务器时的预期日志，不影响功能
- `OpenRouter` 模型加载失败（Failed to fetch）：检查网络与是否配置正确的 API Key/URL
- 直接双击打开本地文件导致请求受限：建议使用本地静态服务器或 Electron 启动
- Windows SmartScreen 提示：安装包未签名为正常现象，可选择“仍要运行”（企业/生产环境建议签名）

---

## 🤝 贡献指南
欢迎提交 Issue 与 Pull Request：
1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/awesome`
3. 提交更改：`git commit -m "feat: add awesome feature"`
4. 推送分支：`git push origin feature/awesome`
5. 发起 Pull Request

---

## 📄 许可证
本项目采用 MIT 许可证，可自由使用、复制、修改与分发（需保留版权与许可证声明）。

---

<div align="center">
  <p>如果这个项目对你有帮助，请给它一个 ⭐️</p>
  <p>Made with ❤️ by Open-GPT Team</p>
</div>
