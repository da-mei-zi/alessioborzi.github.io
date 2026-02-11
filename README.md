# Heng Zhang's Personal Homepage

This is a personal academic homepage based on a YAML configuration system with markdown content files, presented as a modern single-page application.

## 📋 Features

- ✅ Responsive design for desktop and mobile devices
- ✅ Modern single-page application with smooth scrolling
- ✅ YAML-based configuration for easy customization
- ✅ Markdown support for content editing
- ✅ Sections: Home, Awards, Experience, Publications
- ✅ Mathematical equation support with MathJax
- ✅ Bootstrap-based styling

## 🚀 How to Customize

### 1. Edit Configuration File

Edit `contents/config.yml` to update basic information:

```yaml
title: Your Name's Homepage
page-top-title: Your Name
top-section-bg-text: Your motto or tagline
home-subtitle: Your Name
copyright-text: Copyright © 2026 Your Name
```

### 2. Edit Content Files

All content is stored in markdown files in the `contents/` directory:

- `home.md` - Your introduction, contact information, and research interests
- `awards.md` - Your awards and honors
- `experience.md` - Your work and education experience
- `publications.md` - Your research papers and publications

Simply edit these markdown files with your information.

### 3. Modify Navigation Menu 修改导航菜单

The navigation menu appears at the top of every page and contains links like HOME, TEACHING, TALKS, Activities, Research, and OTHERS.

**Files to Edit 需要编辑的文件:**
To change navigation items, you must update ALL 6 HTML files:
要修改导航项，必须更新所有6个HTML文件：

- `index.html`
- `teaching.html`
- `talks.html`
- `travel.html`
- `publications.html`
- `others.html`

**How to Find the Navigation Section 如何找到导航部分:**
- Search for `<nav class="header navbar` in each file
- 在每个文件中搜索 `<nav class="header navbar`
- The navigation section is between `<nav>` and `</nav>` tags
- 导航部分在 `<nav>` 和 `</nav>` 标签之间

**How to Change Navigation Text 如何修改导航文本:**

1. Find the `<nav>` section in each HTML file by searching for `<nav class="header navbar`
   在每个HTML文件中搜索 `<nav class="header navbar` 找到 `<nav>` 部分

2. Look for the navigation items in `<li class="nav-item">` tags
   查找 `<li class="nav-item">` 标签中的导航项

3. Change the text between `<a>` tags to update the menu label
   修改 `<a>` 标签之间的文本来更新菜单标签

Example 示例:
```html
<!-- Before 修改前 -->
<li class="nav-item">
    <a class="nav-link me-lg-3" href="travel.html">TRAVEL</a>
</li>

<!-- After 修改后 -->
<li class="nav-item">
    <a class="nav-link me-lg-3" href="travel.html">Activities</a>
</li>
```

**Important Notes 重要提示:**
- The `active` class makes the navigation item blue on its corresponding page
  `active` 类会使导航项在其对应页面上变为蓝色
- You must update ALL 6 files to keep navigation consistent across pages
  必须更新所有6个文件以保持页面间导航的一致性
- The navigation styling is controlled by CSS selector `#mainNav .navbar-nav .nav-item .nav-link` in `static/css/styles.css`
  导航样式由 `static/css/styles.css` 中的CSS选择器 `#mainNav .navbar-nav .nav-item .nav-link` 控制

### 4. Modify Page Titles 修改页面标题

Each page has a large blue title at the top (e.g., "Activities", "Research").

**Files to Edit 需要编辑的文件:**

- `travel.html` - Activities page title
  活动页面标题
- `publications.html` - Research page title
  研究页面标题
- `teaching.html` - Teaching page title
  教学页面标题
- `talks.html` - Talks page title
  演讲页面标题
- `others.html` - Others page title
  其他页面标题

**How to Find the Page Title 如何找到页面标题:**
- Search for `<h2 id="xxx-subtitle">` in the file (e.g., `id="travel-subtitle"` or `id="publications-subtitle"`)
- 在文件中搜索 `<h2 id="xxx-subtitle">`（例如 `id="travel-subtitle"` 或 `id="publications-subtitle"`）

**How to Change Page Title 如何修改页面标题:**

Find the section header with `<h2 id="xxx-subtitle">` tag and update the text:
找到带有 `<h2 id="xxx-subtitle">` 标签的部分标题并更新文本：

Example 示例:
```html
<!-- Before 修改前 -->
<h2 id="travel-subtitle"><i class="bi bi-airplane-fill"></i> TRAVEL </h2>

<!-- After 修改后 -->
<h2 id="travel-subtitle"><i class="bi bi-airplane-fill"></i> Activities </h2>
```

### 5. Customize Blue Color 自定义蓝色

The blue color used for navigation and titles is defined in CSS:
导航和标题使用的蓝色在CSS中定义：

**File 文件:** `static/css/main.css`

**What to Edit 需要编辑的内容:**
- CSS variable: `--h-title-color:#3948d2;` - Blue color for page titles 页面标题的蓝色
- CSS rule: `.header { border-bottom: solid 2px var(--bs-blue); }` - Navigation border 导航边框

**File 文件:** `static/css/styles.css`

**What to Edit 需要编辑的内容:**
- Selector: `#mainNav .navbar-nav .nav-item .nav-link:hover` - Navigation hover color 导航悬停颜色
- Selector: `#mainNav .navbar-nav .nav-item .nav-link.active` - Navigation active color 导航激活颜色

Example 示例:
```css
/* Change the blue color in main.css 在main.css中修改蓝色 */
:root{
    --h-title-color:#3948d2;  /* Change this hex color value 修改此十六进制颜色值 */
}

/* Change navigation active state in styles.css 在styles.css中修改导航激活状态 */
#mainNav .navbar-nav .nav-item .nav-link.active {
  color: #2937f0;  /* Change this hex color value 修改此十六进制颜色值 */
}
```

### 6. Update Images

Replace the following images in `static/assets/img/`:
- `photo.png` - Your profile photo
- `background.jpeg` - Background image for the top section

### 7. Update Links

To update footer links, search for the `<footer>` section in `index.html` and modify the links as needed.
要更新页脚链接，请在 `index.html` 中搜索 `<footer>` 部分并根据需要修改链接。

## 📁 Directory Structure

```
.
├── contents/           # Content files 内容文件
│   ├── config.yml     # Configuration 配置
│   ├── home.md        # Home section 主页部分
│   ├── awards.md      # Awards section 奖项部分
│   ├── experience.md  # Experience section 经历部分
│   └── publications.md # Publications section 出版物部分
├── static/            # Static assets 静态资源
│   ├── assets/        # Images and favicon 图片和图标
│   ├── css/           # Stylesheets 样式表
│   │   ├── main.css   # Custom styles (colors, layout) 自定义样式（颜色、布局）
│   │   └── styles.css # Bootstrap styles Bootstrap样式
│   └── js/            # JavaScript files JavaScript文件
├── index.html         # Home page 主页
├── teaching.html      # Teaching page 教学页面
├── talks.html         # Talks page 演讲页面
├── travel.html        # Activities page 活动页面
├── publications.html  # Research page 研究页面
└── others.html        # Others page 其他页面
```

## 🎨 Understanding the Structure 理解结构

### HTML Files HTML文件
Each page has the same structure:
每个页面都有相同的结构：

1. **Navigation Bar 导航栏** (inside `<nav>` tag)
   - Contains menu items that link to different pages
   - Location: between `<nav>` and `</nav>` tags
   - 包含链接到不同页面的菜单项
   - 位置：在 `<nav>` 和 `</nav>` 标签之间

2. **Top Section 顶部区域** (class `top-section`)
   - Background image with overlay
   - 带遮罩的背景图片

3. **Photo Avatar 头像照片** (id `avatar`)
   - Profile photo displayed on the page
   - 页面上显示的个人照片

4. **Main Content 主要内容** (inside `<section>` tag)
   - Page-specific content loaded from markdown files
   - 从markdown文件加载的特定页面内容

### CSS Files CSS文件

- **main.css**: Custom styles including:
  - Blue color definitions: CSS variable `--h-title-color`
  - Navigation border: `.header` class styling
  - Page title colors: `section header h2` styling
  - Section backgrounds: `.bg-gradient-primary-to-secondary-*` classes

- **styles.css**: Bootstrap framework styles including:
  - Navigation styles: `#mainNav .navbar-nav .nav-item .nav-link` selectors
  - Responsive design rules
  - Component styles

## 🔧 Quick Reference Guide 快速参考指南

| What to Change 要修改什么 | Files to Edit 编辑的文件 | How to Find 如何查找 |
|------------------------|---------------------|----------------|
| Navigation menu text<br/>导航菜单文本 | All 6 HTML files<br/>所有6个HTML文件 | Search for `<nav>` tag<br/>搜索 `<nav>` 标签 |
| Page titles<br/>页面标题 | Specific HTML file<br/>特定HTML文件 | Search for `id="xxx-subtitle"`<br/>搜索 `id="xxx-subtitle"` |
| Blue colors<br/>蓝色 | main.css, styles.css | Search for: `--h-title-color`, `#mainNav .nav-link.active`<br/>搜索：`--h-title-color`, `#mainNav .nav-link.active` |
| Profile photo<br/>头像 | static/assets/img/photo.png | N/A |
| Content<br/>内容 | contents/*.md | N/A |

## 🌐 Deployment

This website is designed to be deployed on GitHub Pages. Once you push your changes to the repository, GitHub Pages will automatically build and deploy your website.

## 📝 License

This template is based on [Sen Li's academic homepage template](https://github.com/senli1073/senli1073.github.io).

## 👤 Author

**Heng Zhang**
- Email: hengz@mail.ustc.edu.cn
- GitHub: [@Hengz1231](https://github.com/Hengz1231)
- Homepage: [Hengz.github.io](https://Hengz1231.github.io)
