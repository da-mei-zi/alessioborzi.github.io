# 个人主页模板

这是一个简洁美观的个人主页模板，适合学术研究人员、工程师、开发者等使用。

## 📋 模板特点

- ✅ 响应式设计，适配桌面和移动设备
- ✅ 基于 Bootstrap 框架，美观易用
- ✅ 包含多个页面：主页、研究、演讲、活动、教学、链接
- ✅ 支持展示论文、演讲、项目等学术成果
- ✅ 集成社交媒体图标（LinkedIn、GitHub、Google Scholar、arXiv）
- ✅ 自动从 GitHub API 获取最后更新时间

## 🚀 快速开始

### 1. 修改个人信息

按照以下顺序修改各个文件中的内容：

#### 主页 (index.html)
打开 `index.html` 文件，找到带有中文注释的地方进行修改：

1. **页面标题和元数据** (第5-11行)
   - 替换 `Your Name` 为你的名字
   - 替换 `Your Title/Position` 为你的职位
   - 替换 `your-username.github.io` 为你的 GitHub Pages 地址

2. **页面标题栏** (第34-36行)
   - 替换 `你的名字` 为你的真实姓名
   - 替换 `你的职位或身份` 为你的职位描述

3. **个人简介** (第104-126行)
   - 修改个人介绍文字
   - 更新你的教育背景
   - 更新你的工作经历
   - 修改联系邮箱

4. **社交媒体链接** (第129-150行)
   - 更新 LinkedIn 链接
   - 更新 GitHub 链接
   - 更新 Google Scholar 链接（如果没有可以删除）
   - 更新 arXiv 链接（如果不需要可以删除）

5. **最后更新脚本** (第72-95行)
   - 替换 `your-username.github.io` 为你的仓库名
   - 替换 `your-github-username` 为你的 GitHub 用户名

#### 研究页面 (research.html)

1. 修改页面标题和名字（第5行、第28-29行）
2. 修改研究兴趣（第68行）
3. 添加你的预印本论文（第74-95行）
   - 每篇论文是一个 `<tr>` 行
   - 复制模板添加更多论文
4. 添加你的已发表论文（第100-143行）
   - 包含论文标题、期刊/会议名称、年份、作者、链接

#### 演讲页面 (talks.html)

1. 修改页面标题和名字
2. 添加你的演讲记录（第69-97行）
   - 包含演讲标题、地点、日期
   - 可以添加幻灯片和视频链接
3. 添加海报展示（第102-114行）

#### 活动页面 (activities.html)

1. 修改页面标题和名字
2. 列出你组织的活动（第69-75行）
3. 列出即将参加的活动（第80-104行）
4. 列出参加过的活动（第109-142行）

#### 教学页面 (teaching.html)

1. 修改页面标题和名字
2. 列出你的教学经历（第70-77行）
3. 可以添加指导学生项目等内容

#### 链接页面 (links.html)

1. 修改页面标题和名字
2. 添加读书小组和研讨会链接（第67-72行）
3. 列出你的合作者（第77-82行）
4. 列出你的会员资格（第88-93行）
5. 添加学位论文链接（第99-104行）
6. 分享学习笔记（第110-116行）

### 2. 替换个人照片

1. 准备一张你的照片（推荐尺寸：400x400像素或更大，正方形）
2. 将照片命名为 `profile.png` 或 `profile.jpg`
3. 将照片放入 `images/` 文件夹
4. 如果使用 .jpg 格式，需要在 `index.html` 中修改图片扩展名（第122行）

### 3. 添加文件（可选）

如果你有以下文件，可以添加到对应文件夹：

- **简历 PDF**: 放入 `pdf/cv/` 文件夹，命名为 `CV.pdf`
- **论文 PDF**: 放入 `pdf/thesis/` 文件夹
- **演讲幻灯片**: 放入 `slides/` 文件夹
- **海报**: 放入 `poster/` 文件夹
- **笔记**: 放入 `pdf/notes/` 文件夹

### 4. 部署到 GitHub Pages

#### 方法一：使用现有仓库

如果这个仓库已经是你的 GitHub Pages 仓库：

1. 确保仓库名称格式为：`your-username.github.io`
2. 将所有修改提交到 `main` 或 `master` 分支
3. 在仓库设置中启用 GitHub Pages
4. 访问 `https://your-username.github.io` 查看结果

#### 方法二：创建新仓库

1. 在 GitHub 创建新仓库，命名为：`your-username.github.io`
2. 将这个模板的所有文件复制到新仓库
3. 推送到 GitHub：
   ```bash
   git add .
   git commit -m "Initial commit: Personal homepage"
   git push origin main
   ```
4. 在仓库设置中启用 GitHub Pages，选择 `main` 分支的根目录
5. 等待几分钟，访问 `https://your-username.github.io`

## 📁 文件结构

```
.
├── index.html          # 主页
├── research.html       # 研究页面
├── talks.html          # 演讲页面
├── activities.html     # 活动页面
├── teaching.html       # 教学页面
├── links.html          # 链接页面
├── css/                # 样式文件
│   ├── bootstrap.min.css
│   └── style.css
├── js/                 # JavaScript 文件
│   ├── jquery-3.5.1.min.js
│   └── bootstrap.min.js
├── images/             # 图片文件夹
│   ├── profile.png     # 你的个人照片（需要替换）
│   └── mathbackground.png
├── icons/              # 社交媒体图标
├── pdf/                # PDF 文件
│   ├── cv/            # 简历
│   ├── thesis/        # 论文
│   └── notes/         # 笔记
├── slides/             # 演讲幻灯片
├── poster/             # 海报
└── README.md          # 本说明文件
```

## 🎨 自定义样式

如果你想修改网站的颜色、字体等样式：

1. 打开 `css/style.css` 文件
2. 修改其中的 CSS 规则
3. 常见修改项：
   - 背景颜色
   - 标题颜色
   - 链接颜色
   - 字体大小

## 💡 使用技巧

### 添加新的导航页面

如果你想添加新的页面（比如"项目"页面）：

1. 复制一个现有的 HTML 文件（如 `research.html`）
2. 重命名为新的名字（如 `projects.html`）
3. 修改页面内容
4. 在所有页面的导航栏中添加链接：
   ```html
   <li class="nav-item"><a class="nav-link" href="./projects.html">Projects</a></li>
   ```

### 删除不需要的页面

如果你不需要某个页面（比如"教学"页面）：

1. 删除对应的 HTML 文件
2. 在所有页面的导航栏中删除对应的链接

### 修改导航栏

导航栏代码在每个 HTML 文件的第46-64行，你可以：
- 删除不需要的导航项
- 修改导航项的顺序
- 添加新的导航项

## ❓ 常见问题

### Q: 如何修改网站的颜色主题？
A: 编辑 `css/style.css` 文件，修改颜色值。

### Q: 如何添加更多社交媒体图标？
A: 在 `index.html` 的第125-152行添加新的 `<td>` 标签，并在 `icons/` 文件夹中添加对应图标。

### Q: 网站没有正确显示怎么办？
A: 检查：
1. 所有 HTML 文件中的链接是否正确
2. 图片文件是否存在
3. GitHub Pages 是否已启用
4. 浏览器控制台是否有错误信息

### Q: 如何测试网站？
A: 在本地打开 `index.html` 文件，或者使用本地服务器：
```bash
# 使用 Python
python -m http.server 8000

# 然后访问 http://localhost:8000
```

## 📞 需要帮助？

如果你在使用过程中遇到问题：
1. 检查浏览器控制台的错误信息
2. 确保所有文件路径正确
3. 确保 HTML 语法正确（特别是标签要闭合）

## 📄 许可

这是一个开源模板，你可以自由使用和修改。

---

**祝你使用愉快！** 🎉

如果这个模板对你有帮助，欢迎给项目加星⭐
