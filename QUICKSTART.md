# 🚀 快速开始指南

## 最快 30 秒开始使用

### 方式 1：直接打开（推荐）

1. 下载 `index.html` 文件
2. 双击打开或用浏览器打开
3. 开始聊天！

**就这么简单！** 无需任何安装或配置。

### 方式 2：在线访问

访问：https://ai.661015.xuz

### 方式 3：本地服务器

```bash
# 进入项目目录
cd ai-chat-html-repo

# 启动本地服务器
python -m http.server 8000

# 访问 http://localhost:8000
```

## 🎯 常见操作

### 创建新对话
点击左侧 **+ 新建对话** 按钮

### 切换语言
点击右上角的 **中文** 或 **EN** 按钮

### 发送消息
1. 在底部输入框输入问题
2. 按 **Enter** 或点击 **发送** 按钮
3. 等待 AI 回复

### 查看对话历史
左侧边栏显示所有对话，点击即可切换

### 清空对话
在对话中输入内容后，底部会显示清空按钮

## 💡 使用技巧

### 快捷键
- **Enter**：发送消息
- **Shift+Enter**：换行

### 性能优化
- 应用会自动保存对话历史
- 刷新页面不会丢失对话
- 支持离线使用（已加载的对话）

### 移动端使用
- 完全响应式设计
- 自动隐藏侧边栏
- 优化的触摸体验

## ❓ 常见问题

### Q: 需要安装什么吗？
A: 不需要！直接打开 HTML 文件即可使用。

### Q: 需要网络连接吗？
A: 需要。应用需要网络连接才能与 AI 通信。

### Q: 我的对话会被保存吗？
A: 会的！对话保存在浏览器本地存储中。

### Q: 支持哪些浏览器？
A: 支持所有现代浏览器（Chrome、Firefox、Safari、Edge 等）。

### Q: 如何修改 API Key？
A: 编辑 `index.html` 文件，找到 `const API_KEY = '...'` 这一行，修改即可。

### Q: 如何自定义颜色？
A: 编辑 `index.html` 中的 CSS 部分，修改颜色值即可。

### Q: 支持文件上传吗？
A: 当前版本不支持，可以在未来版本中添加。

## 🎨 自定义配置

### 修改 API Key

打开 `index.html`，找到这一行：

```javascript
const API_KEY = 'sk-c3gs45vbc6ha1qs0akck494k9eerv7snmtydzbx6l0zkbf2w';
```

替换为你的 API Key。

### 修改颜色方案

在 `<style>` 部分找到颜色定义：

```css
/* 修改这些颜色 */
--neon-cyan: #00d4ff;      /* 青色 */
--neon-pink: #ff006e;      /* 粉色 */
--neon-purple: #8338ec;    /* 紫色 */
--neon-yellow: #ffbe0b;    /* 黄色 */
--neon-orange: #fb5607;    /* 橙色 */
```

### 修改应用标题

找到这一行：

```html
<h1>AI 聊天助手 Pro</h1>
```

修改为你想要的标题。

## 🚀 部署到自己的服务器

### GitHub Pages

1. Fork 此仓库
2. 编辑 `CNAME` 文件，输入你的域名
3. 在 GitHub 设置中启用 Pages
4. 配置 DNS 记录

### 其他服务器

1. 上传 `index.html` 到你的服务器
2. 配置 DNS 指向你的服务器
3. 完成！

## 📞 获取帮助

- 📖 查看 [完整文档](README.md)
- 🐛 报告 Bug：[GitHub Issues](https://github.com/yel893182-cell/ai-chat-html/issues)
- 💬 提出建议：[GitHub Discussions](https://github.com/yel893182-cell/ai-chat-html/discussions)

## 🎉 开始使用吧！

现在你已经准备好了。选择上面的任何一种方式，立即开始使用 AI 聊天助手吧！

**祝你使用愉快！** 🚀
