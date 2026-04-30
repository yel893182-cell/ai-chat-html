# 🚀 AI 聊天助手 Pro - 超级炫彩版

一个功能完善、视觉震撼的 AI 聊天应用。采用现代化设计和酷炫特效，支持多语言、实时聊天、消息管理等完整功能。

![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

## ✨ 核心特性

### 🎨 超级炫彩设计
- **粒子系统背景**：实时流动的彩色粒子和连接线动画
- **炫彩渐变配色**：青/粉/紫/黄/橙五色渐变配色系统
- **发光脉冲效果**：按钮、头像、标题的持续脉冲发光
- **玻璃态设计**：毛玻璃背景 + 透明度渐变效果
- **流光特效**：边框和输入框的流动光线动画
- **文本渐变**：标题和重要文本的彩色渐变效果

### 💬 完整聊天功能
- **实时消息**：集成 xiaomimimo API，支持流畅的消息交互
- **消息历史**：自动保存所有对话记录
- **多对话管理**：支持创建、切换、删除多个独立对话
- **消息操作**：复制、清空、删除等完整操作
- **API 集成**：已内置 API Key，无需配置

### 🌐 国际化支持
- **双语言切换**：中文/English 无缝切换
- **语言偏好保存**：自动记住用户语言选择
- **完整翻译**：所有界面文本都支持双语言

### 📱 响应式设计
- **移动端优化**：完美适配手机、平板、桌面
- **触摸友好**：优化的移动端交互体验
- **自适应布局**：智能响应不同屏幕尺寸

## 🎯 快速开始

### 方式 1：直接打开（最简单）

1. 下载 `index.html` 文件
2. 用浏览器打开即可使用
3. 无需任何安装或配置

### 方式 2：在线访问

访问 GitHub Pages：`https://ai.661015.xuz`

### 方式 3：本地服务器

```bash
# 使用 Python 3
python -m http.server 8000

# 或使用 Node.js
npx http-server

# 然后访问 http://localhost:8000
```

## 📁 项目结构

```
ai-chat-html-repo/
├── index.html          # 主应用文件（包含所有代码）
├── README.md           # 项目文档
├── QUICKSTART.md       # 快速开始指南
├── DEPLOYMENT.md       # 部署指南
├── LICENSE             # MIT 许可证
└── CNAME               # GitHub Pages 自定义域名配置
```

## 🎨 设计系统

### 颜色方案
- **主背景**：`#0a0e27`（深蓝黑）
- **卡片背景**：`#1a1f3a`（深紫蓝）
- **强调色**：
  - 青色：`#00d4ff`
  - 粉色：`#ff006e`
  - 紫色：`#8338ec`
  - 黄色：`#ffbe0b`
  - 橙色：`#fb5607`

### 特效类名
- `.glow-pulse` - 脉冲发光效果
- `.message-content` - 消息卡片样式
- `.float` - 浮动动画
- `.slideIn` - 滑入动画

## 🔧 技术栈

| 技术 | 说明 |
|------|------|
| HTML5 | 标记语言 |
| CSS3 | 样式和动画 |
| JavaScript | 交互逻辑 |
| Canvas API | 粒子系统 |
| Fetch API | HTTP 请求 |

## 🚀 部署指南

### GitHub Pages 部署

1. **Fork 或克隆此仓库**
   ```bash
   git clone https://github.com/yel893182-cell/ai-chat-html.git
   cd ai-chat-html
   ```

2. **配置自定义域名**
   - 编辑 `CNAME` 文件
   - 输入你的域名：`ai.661015.xuz`

3. **推送到 GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

4. **启用 GitHub Pages**
   - 进入仓库设置
   - 在 Pages 部分选择 main 分支
   - 配置自定义域名

5. **配置 DNS**
   - 在你的域名提供商处配置 DNS 记录
   - 添加 CNAME 记录指向 GitHub Pages

### 其他部署方式

#### Vercel 部署
```bash
vercel --prod
```

#### Netlify 部署
```bash
netlify deploy --prod --dir=.
```

#### 自托管部署
```bash
# 上传 index.html 到你的服务器
scp index.html user@your-server:/var/www/html/
```

## 📖 使用说明

### 基本操作

1. **创建新对话**
   - 点击左侧 "新建对话" 按钮

2. **切换语言**
   - 点击右上角 "中文" 或 "EN" 按钮

3. **发送消息**
   - 在输入框输入问题
   - 按 Enter 或点击发送按钮

4. **查看历史**
   - 左侧边栏显示所有对话
   - 点击即可切换对话

### 快捷键

| 快捷键 | 功能 |
|--------|------|
| Enter | 发送消息 |
| Shift+Enter | 换行 |

## 🎓 学习资源

- [HTML5 MDN 文档](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS3 MDN 文档](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript MDN 文档](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Canvas API 文档](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📝 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

## 💬 反馈和支持

- 🐛 Bug 报告: [GitHub Issues](https://github.com/yel893182-cell/ai-chat-html/issues)
- 💡 功能建议: [GitHub Discussions](https://github.com/yel893182-cell/ai-chat-html/discussions)

## 🎉 致谢

感谢所有贡献者和使用者的支持！

---

**⭐ 如果你喜欢这个项目，请给个 Star！**

**🚀 开始使用：** [访问应用](https://ai.661015.xuz)
