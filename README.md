# White Navigation Page | 白色导航页

[![Modern Web Guidance](https://img.shields.io/badge/Modern%20Web%20Guidance-GoogleChrome-4285F4?logo=googlechrome&logoColor=white)](https://github.com/GoogleChrome/modern-web-guidance)

![](https://cdn.jsdelivr.net/gh/pusvsimg/img@main/Image/20250102110532172.png)

![](https://cdn.jsdelivr.net/gh/pusvsimg/img@main/Image/20250102110609237.png)

[English](#english) | [中文](#chinese)

## English

A clean and elegant website navigation page with Neumorphism design.

### Features

- 🎨 Neumorphism Design
- 🌓 Dark/Light Mode Toggle
- 🔍 Real-time Search
- 📱 Responsive Layout
- ♿ Accessible by Design (keyboard navigation, screen reader support)
- 🗂️ Categorized Display
  - Search Engines & Social Media
  - E-commerce & Shopping
  - Entertainment & Streaming
  - News & Information
  - Productivity & Tools

### Tech Stack

- HTML5
- CSS3
- JavaScript (Vanilla JS, no framework needed)
- Font Awesome Icons
- Google Fonts
- [Modern Web Guidance](https://github.com/GoogleChrome/modern-web-guidance) (modern web best practices)

### Modern Web Guidance

This project has been audited and optimized against [Modern Web Guidance](https://github.com/GoogleChrome/modern-web-guidance), Google Chrome's set of skills that embeds web platform expertise, best practices, and browser compatibility data directly into coding agents. The visual design and interactions are intentionally left unchanged.

Applied guidance includes:

- **Accessibility**: semantic landmarks, real links and lists, accessible labels, `aria-live` search results, and `aria-pressed` toggle buttons
- **HTML**: `<!DOCTYPE html>`, `lang`, charset, viewport, and native `<search>` / `<footer>` elements
- **Dark mode**: unchanged manual light/dark toggle
- **Secure external resources**: Subresource Integrity (SRI), `crossorigin`, `referrerpolicy`, and `rel="noopener noreferrer"`
- **Performance**: DocumentFragment rendering to avoid layout thrash during initial render

Run the same checks locally:

```bash
# Scan for legacy patterns to modernize
npx modern-web-guidance@latest legacy-scan .

# Search and retrieve a specific guide
npx modern-web-guidance@latest search "accessible dark mode"
```

### Quick Start

1. Clone the repository
```bash
git clone https://github.com/yourusername/white-navigation.git
```

2. Preview locally
```bash
# Using Python local server
python -m http.server 8000

# Or using Node.js http-server
npx http-server
```

3. Visit `http://localhost:8000` in your browser

### Deployment

#### Method 1: GitHub Pages

1. Fork this repository to your GitHub account

2. Rename the repository to `yourusername.github.io`
   - Go to repository Settings
   - Change repository name

3. Enable GitHub Pages
   - Go to repository Settings
   - Find Pages section
   - Select main branch as Source
   - Wait a few minutes after saving

4. Visit `https://yourusername.github.io` to see your deployed site

5. Custom Domain Setup (Optional)
   - Go to repository Settings > Pages
   - In the "Custom domain" section, enter your domain
   - Add DNS records at your domain provider:
     ```
     Type: A
     Name: @
     Value: 185.199.108.153
           185.199.109.153
           185.199.110.153
           185.199.111.153
     ```
     Or for a subdomain:
     ```
     Type: CNAME
     Name: www
     Value: yourusername.github.io
     ```
   - Wait for DNS propagation (usually 24-48 hours)
   - Check "Enforce HTTPS" for secure access

#### Method 2: Cloudflare Pages

1. Sign up/Log in to Cloudflare

2. Go to Pages dashboard
   - Click "Create a project"
   - Choose "Connect to Git"

3. Configure deployment
   - Select your repository
   - Set build configuration:
     - Build command: leave empty (no build needed)
     - Output directory: `/`
     - Environment variables: none needed

4. Deploy settings
   - Branch: main
   - Build settings: keep default
   - Click "Save and Deploy"

5. Wait for deployment
   - Cloudflare will assign a domain (format: your-project.pages.dev)
   - Custom Domain Setup (Optional):
     1. Go to your project's settings
     2. Click on "Custom domains"
     3. Click "Set up a custom domain"
     4. Enter your domain name
     5. Follow one of these methods:
        - Method A: Use Cloudflare as DNS provider
          * Transfer your domain to Cloudflare (recommended)
          * DNS records will be configured automatically
        - Method B: Use another DNS provider
          * Add a CNAME record:
            ```
            Type: CNAME
            Name: @
            Value: your-project.pages.dev
            ```
     6. Wait for SSL certificate provisioning
     7. Domain will be active with HTTPS enabled

### Customization

#### Adding New Websites

Find the `websites` array in `index.html` and add new websites in this format:

```javascript
{
  name: "Website Name",
  icon: "fab fa-icon-name",  // Font Awesome icon class
  url: "https://website.com",
  category: "categoryName"  // Choose from existing categories
}
```

#### Modifying Styles

Color tokens are defined in the `:root` selector, and the dark theme overrides them on `body.dark-mode`:

```css
:root {
  --primary-color: #6200ee;
  --background-color: #e0e5ec;
  --surface-color: #e0e5ec;
  /* other tokens... */
}

body.dark-mode {
  --background-color: #1a1a1a;
  --surface-color: #2a2a2a;
  /* other tokens... */
}
```

The page loads in the light theme by default; the theme toggle switches to dark by adding the `dark-mode` class to `<body>`.

### Contributing

Issues and Pull Requests are welcome to improve this project.

### License

This project is licensed under the MIT License.

---

## Chinese

一个简洁优雅的网址导航页面，采用新拟物设计风格（Neumorphism）。

### 特性

- 🎨 新拟物设计风格
- 🌓 深色/浅色模式切换
- 🔍 实时搜索功能
- 📱 响应式布局
- ♿ 无障碍支持（键盘导航、屏幕阅读器）
- 🗂️ 分类展示
  - 搜索引擎和社交媒体
  - 电子商务和购物
  - 娱乐和流媒体
  - 新闻和资讯
  - 生产力和工具

### 技术栈

- HTML5
- CSS3
- JavaScript (原生JS，无需框架)
- Font Awesome 图标
- Google Fonts
- [Modern Web Guidance](https://github.com/GoogleChrome/modern-web-guidance)（现代 Web 最佳实践）

### Modern Web Guidance

本项目已按照 [Modern Web Guidance](https://github.com/GoogleChrome/modern-web-guidance) 完成审查与优化。该指南由 Google Chrome 团队维护，将 Web 平台专业知识、最佳实践与浏览器兼容性数据直接注入编码智能体。页面视觉与交互保持不变。

已应用的指南包括：

- **无障碍**：语义化地标、真实链接与列表、可访问标签、`aria-live` 搜索结果与 `aria-pressed` 切换按钮
- **HTML**：`<!DOCTYPE html>`、`lang`、charset、viewport，以及原生 `<search>` / `<footer>` 元素
- **深色模式**：保持原有的手动深色/浅色切换
- **外部资源安全**：Subresource Integrity (SRI)、`crossorigin`、`referrerpolicy` 与 `rel="noopener noreferrer"`
- **性能**：使用 DocumentFragment 渲染，避免初次渲染时的布局抖动

本地运行同样的检查：

```bash
# 扫描需要现代化的旧模式
npx modern-web-guidance@latest legacy-scan .

# 搜索并检索具体指南
npx modern-web-guidance@latest search "accessible dark mode"
```

### 快速开始

1. 克隆仓库
```bash
git clone https://github.com/yourusername/white-navigation.git
```

2. 本地预览
```bash
# 使用Python启动本地服务器
python -m http.server 8000

# 或使用Node.js的http-server
npx http-server
```

3. 在浏览器中访问 `http://localhost:8000`

### 部署方式

#### 方式一：GitHub Pages 部署

1. Fork 本仓库到你的GitHub账号下

2. 修改仓库名为 `yourusername.github.io`
   - 进入仓库设置 Settings
   - 修改仓库名称

3. 启用 GitHub Pages
   - 进入仓库设置 Settings
   - 找到 Pages 选项
   - Source 选择 main 分支
   - 保存后等待几分钟

4. 访问 `https://yourusername.github.io` 即可看到部署好的网站

5. 自定义域名设置（可选）
   - 进入仓库设置 Settings > Pages
   - 在"Custom domain"部分输入您的域名
   - 在您的域名提供商添加 DNS 记录：
     ```
     类型: A
     主机记录: @
     值: 185.199.108.153
        185.199.109.153
        185.199.110.153
        185.199.111.153
     ```
     或者对于子域名：
     ```
     类型: CNAME
     主机记录: www
     值: yourusername.github.io
     ```
   - 等待 DNS 解析生效（通常需要24-48小时）
   - 勾选"Enforce HTTPS"以启用安全访问

#### 方式二：Cloudflare Pages 部署

1. 注册 Cloudflare 账号并登录

2. 进入 Pages 面板
   - 点击 "Create a project"
   - 选择 "Connect to Git"

3. 配置部署
   - 选择你的代码仓库
   - 设置构建配置：
     - 构建命令：留空（无需构建）
     - 输出目录：填写 `/`
     - 环境变量：无需设置

4. 部署设置
   - 分支：main
   - 构建设置：保持默认
   - 点击 "Save and Deploy"

5. 等待部署完成
   - Cloudflare 会自动分配一个域名（格式如：your-project.pages.dev）
   - 自定义域名设置（可选）：
     1. 进入项目设置
     2. 点击"Custom domains"
     3. 点击"Set up a custom domain"
     4. 输入您的域名
     5. 选择以下任一方式：
        - 方式A：使用 Cloudflare 作为 DNS 提供商
          * 将域名转入 Cloudflare（推荐）
          * DNS 记录将自动配置
        - 方式B：使用其他 DNS 提供商
          * 添加 CNAME 记录：
            ```
            类型: CNAME
            主机记录: @
            值: your-project.pages.dev
            ```
     6. 等待 SSL 证书配置完成
     7. 域名将启用 HTTPS 并生效

### 自定义修改

#### 添加新网站

在 `index.html` 文件中找到 `websites` 数组，按照以下格式添加新网站：

```javascript
{
  name: "网站名称",
  icon: "fab fa-icon-name",  // Font Awesome图标类名
  url: "https://website.com",
  category: "分类名称"  // 从已有分类中选择
}
```

#### 修改样式

颜色令牌在 `:root` 选择器中定义，深色主题则在 `body.dark-mode` 上覆盖：

```css
:root {
  --primary-color: #6200ee;
  --background-color: #e0e5ec;
  --surface-color: #e0e5ec;
  /* 其他令牌... */
}

body.dark-mode {
  --background-color: #1a1a1a;
  --surface-color: #2a2a2a;
  /* 其他令牌... */
}
```

页面默认使用浅色主题；主题切换按钮通过为 `<body>` 添加 `dark-mode` 类切换到深色。

### 贡献

欢迎提交 Issue 和 Pull Request 来改进这个项目。

### 许可证

本项目采用 MIT 许可证。
