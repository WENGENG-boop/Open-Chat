# Open-GPT

<div align="center">
  <h3>🤖 一个现代化的AI聊天应用</h3>
  <p>基于Electron构建的跨平台AI聊天客户端，支持多种AI模型</p>
  
  ![License](https://img.shields.io/badge/license-MIT-blue.svg)
  ![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey.svg)
  ![Electron](https://img.shields.io/badge/Electron-27.0.0-47848f.svg)
  ![Vue.js](https://img.shields.io/badge/Vue.js-3.3.11-4fc08d.svg)
</div>

## ✨ 功能特性

- 🎯 **多模型支持** - 支持OpenAI、OpenRouter等多种AI服务提供商
- 💬 **智能对话** - 流式响应，实时显示AI思考过程
- 📱 **响应式设计** - 适配桌面和移动端界面
- 🔧 **自定义配置** - 支持自定义API、模型和系统提示词
- 📚 **历史记录** - 本地保存对话历史，支持快速切换
- 🎨 **现代UI** - 基于Tailwind CSS的美观界面
- ⚡ **快速启动** - 一键安装，开箱即用

## 🚀 快速开始

### 方式一：下载安装包（推荐）

1. 前往 [Releases](../../releases) 页面下载最新版本
2. 下载 `Open-GPT Setup 1.0.0.exe`（Windows）
3. 双击运行安装程序
4. 按照安装向导完成安装
5. 启动应用并配置API密钥

### 方式二：从源码运行

```bash
# 克隆仓库
git clone https://github.com/your-username/open-gpt.git
cd open-gpt

# 安装依赖
npm install

# 启动应用
npm start

# 构建安装包
npm run dist
```

## ⚙️ 配置说明

### API配置

1. 点击右上角设置图标
2. 选择API提供商：
   - **OpenAI**: 使用官方OpenAI API
   - **OpenRouter**: 使用OpenRouter聚合服务
   - **自定义**: 配置自己的API端点
3. 输入对应的API Key
4. 选择合适的AI模型

### 支持的模型

#### OpenAI 模型
- GPT-3.5 Turbo
- GPT-4
- GPT-4 Turbo
- GPT-4o
- GPT-4o Mini

#### OpenRouter 模型
- 支持100+种开源和商业模型
- 自动区分免费和付费模型
- 实时显示模型定价信息

## 🛠️ 技术栈

- **前端框架**: Vue.js 3.3.11
- **桌面框架**: Electron 27.0.0
- **UI框架**: Tailwind CSS
- **Markdown渲染**: Marked.js
- **图标库**: Font Awesome
- **构建工具**: electron-builder

## 📁 项目结构

```
open-gpt/
├── index (1).html          # 主页面文件
├── main.js                 # Electron主进程
├── package.json            # 项目配置
├── dist/                   # 构建输出目录
│   ├── Open-GPT Setup 1.0.0.exe  # Windows安装包
│   └── win-unpacked/       # 未打包的应用文件
├── images.png              # 应用图标
└── README.md              # 项目说明
```

## 🎯 使用指南

### 基本对话
1. 在底部输入框输入问题
2. 按Enter或点击发送按钮
3. 等待AI响应，支持实时流式显示

### 历史记录
1. 点击左上角菜单图标打开侧边栏
2. 查看历史对话记录
3. 点击任意历史记录快速切换

### 新建对话
1. 点击顶部的"+"图标
2. 开始新的对话会话

## 🤝 贡献指南

欢迎提交Issue和Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开Pull Request

## 📝 更新日志

### v1.0.0 (2024-01-09)
- ✨ 初始版本发布
- 🎯 支持多种AI模型
- 💬 实现流式对话
- 📱 响应式界面设计
- 🔧 完整的配置系统

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 💬 反馈与支持

- 📧 邮箱: yizheng.weng404@gmail.com
- 🐛 问题反馈: [Issues](../../issues)
- 💡 功能建议: [Discussions](../../discussions)

---

<div align="center">
  <p>如果这个项目对你有帮助，请给它一个 ⭐️</p>
  <p>Made with ❤️ by Open-GPT Team</p>
</div>
