# 🚀 部署指南

本文档介绍如何将 AI 聊天助手部署到各种平台。

## 📋 前置要求

- 一个 HTML 文件（`index.html`）
- 一个域名（可选，但推荐）
- 基本的 Git 知识（可选）

## 🌐 GitHub Pages 部署（推荐）

### 优势
- ✅ 完全免费
- ✅ 自动 HTTPS
- ✅ 自定义域名支持
- ✅ 无需维护服务器

### 部署步骤

#### 步骤 1：创建 GitHub 仓库

1. 登录 GitHub
2. 创建新仓库 `ai-chat-html`
3. 选择 Public（公开）

#### 步骤 2：上传文件

```bash
# 克隆仓库
git clone https://github.com/YOUR_USERNAME/ai-chat-html.git
cd ai-chat-html

# 复制 index.html 到仓库
cp /path/to/index.html .

# 添加文件
git add .
git commit -m "Initial commit: Add AI chat application"
git push origin main
```

#### 步骤 3：启用 GitHub Pages

1. 进入仓库设置（Settings）
2. 左侧菜单选择 "Pages"
3. 在 "Build and deployment" 部分：
   - Source 选择 "Deploy from a branch"
   - Branch 选择 "main" 和 "/ (root)"
4. 点击 Save

#### 步骤 4：配置自定义域名（可选）

1. 在 GitHub Pages 设置中，找到 "Custom domain"
2. 输入你的域名：`ai.661015.xuz`
3. 点击 Save

**GitHub 会自动创建 `CNAME` 文件**

#### 步骤 5：配置 DNS 记录

在你的域名提供商（如阿里云、腾讯云、Cloudflare 等）处：

1. 添加 CNAME 记录
2. 名称：`ai`
3. 值：`YOUR_USERNAME.github.io`
4. 保存

**等待 DNS 生效（通常 10-30 分钟）**

### 验证部署

访问 `https://ai.661015.xuz`，应该能看到你的应用。

## 🚀 Vercel 部署

### 优势
- ✅ 一键部署
- ✅ 自动 HTTPS
- ✅ 全球 CDN
- ✅ 自定义域名支持

### 部署步骤

1. **访问 Vercel**
   - 进入 [vercel.com](https://vercel.com)
   - 用 GitHub 账户登录

2. **导入项目**
   - 点击 "New Project"
   - 选择你的 GitHub 仓库

3. **配置**
   - Framework Preset: "Other"
   - Build Command: 留空
   - Output Directory: `.`

4. **部署**
   - 点击 "Deploy"
   - 等待部署完成

5. **配置自定义域名**
   - 进入项目设置
   - 选择 "Domains"
   - 添加 `ai.661015.xuz`
   - 按照说明配置 DNS

## 🌐 Netlify 部署

### 优势
- ✅ 免费托管
- ✅ 简单的 Git 集成
- ✅ 自动部署
- ✅ 自定义域名支持

### 部署步骤

1. **访问 Netlify**
   - 进入 [netlify.com](https://netlify.com)
   - 用 GitHub 账户登录

2. **创建新站点**
   - 点击 "New site from Git"
   - 选择你的 GitHub 仓库

3. **配置构建**
   - Build command: 留空
   - Publish directory: `.`

4. **部署**
   - 点击 "Deploy site"
   - 等待部署完成

5. **配置自定义域名**
   - 进入 Site settings
   - 选择 "Domain management"
   - 添加自定义域名
   - 按照说明配置 DNS

## 🖥️ 自托管部署

### 在 Linux 服务器上部署

#### 使用 Nginx

1. **安装 Nginx**
   ```bash
   sudo apt-get update
   sudo apt-get install nginx
   ```

2. **上传文件**
   ```bash
   scp index.html user@your-server:/var/www/html/
   ```

3. **配置 Nginx**
   ```bash
   sudo nano /etc/nginx/sites-available/default
   ```

   添加配置：
   ```nginx
   server {
       listen 80;
       server_name ai.661015.xuz;

       location / {
           root /var/www/html;
           try_files $uri $uri/ =404;
       }
   }
   ```

4. **重启 Nginx**
   ```bash
   sudo systemctl restart nginx
   ```

5. **配置 SSL（HTTPS）**
   ```bash
   sudo apt-get install certbot python3-certbot-nginx
   sudo certbot --nginx -d ai.661015.xuz
   ```

#### 使用 Apache

1. **安装 Apache**
   ```bash
   sudo apt-get install apache2
   ```

2. **上传文件**
   ```bash
   scp index.html user@your-server:/var/www/html/
   ```

3. **启用 mod_rewrite**
   ```bash
   sudo a2enmod rewrite
   ```

4. **配置虚拟主机**
   ```bash
   sudo nano /etc/apache2/sites-available/ai.conf
   ```

   添加配置：
   ```apache
   <VirtualHost *:80>
       ServerName ai.661015.xuz
       DocumentRoot /var/www/html

       <Directory /var/www/html>
           Options Indexes FollowSymLinks
           AllowOverride All
           Require all granted
       </Directory>
   </VirtualHost>
   ```

5. **启用站点**
   ```bash
   sudo a2ensite ai.conf
   sudo systemctl restart apache2
   ```

## 🐳 Docker 部署

### Dockerfile

```dockerfile
FROM nginx:alpine

# 复制 HTML 文件
COPY index.html /usr/share/nginx/html/

# 复制 Nginx 配置
COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
```

### 构建和运行

```bash
# 构建镜像
docker build -t ai-chat:latest .

# 运行容器
docker run -p 80:80 ai-chat:latest
```

## 🔒 安全建议

### HTTPS 配置
- 始终使用 HTTPS
- 配置 HSTS 头
- 定期更新 SSL 证书

### API Key 安全
- 不要在公开仓库中暴露真实的 API Key
- 考虑在后端代理 API 请求
- 定期轮换 API Key

### 内容安全策略 (CSP)
```html
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline'">
```

## 📊 监控和日志

### GitHub Pages
- 查看部署日志：仓库 → Actions
- 查看错误：浏览器开发者工具

### Vercel
- 实时日志：项目 → Deployments
- 性能监控：项目 → Analytics

### 自托住
```bash
# Nginx 日志
tail -f /var/log/nginx/access.log
tail -f /var/log/nginx/error.log

# Apache 日志
tail -f /var/log/apache2/access.log
tail -f /var/log/apache2/error.log
```

## 🆘 故障排除

### 域名无法访问
- 检查 DNS 配置是否正确
- 检查 DNS 是否已生效（使用 `nslookup` 或 `dig`）
- 等待 DNS 缓存过期（通常 24 小时）

### 页面加载缓慢
- 启用 gzip 压缩
- 使用 CDN
- 优化资源大小

### API 请求失败
- 检查 API Key 是否有效
- 检查网络连接
- 检查浏览器控制台错误

### HTTPS 证书错误
- 确保域名正确配置
- 重新生成 SSL 证书
- 清除浏览器缓存

## 📚 更多资源

- [GitHub Pages 文档](https://pages.github.com)
- [Vercel 文档](https://vercel.com/docs)
- [Netlify 文档](https://docs.netlify.com)
- [Nginx 文档](https://nginx.org/en/docs/)
- [Apache 文档](https://httpd.apache.org/docs/)

---

**需要帮助？** 查看 [快速开始指南](QUICKSTART.md) 或提交 Issue
