# GitHub Pages 部署指南

本指南将帮助你将个人主页部署到 GitHub Pages，让全世界都能访问你的网站。

## 🌐 什么是 GitHub Pages？

GitHub Pages 是 GitHub 提供的免费静态网站托管服务，你可以用它来托管个人主页、项目文档等。

## 📋 部署前准备

在开始部署之前，请确保你已经：

1. ✅ 完成了 README.md 中的所有个人信息修改
2. ✅ 替换了个人照片
3. ✅ 删除或修改了所有示例内容
4. ✅ 在本地测试过网站（使用 `python -m http.server`）

## 🚀 部署步骤

### 方法一：使用现有仓库（推荐）

如果你是通过 fork 或 clone 了这个仓库：

#### 步骤 1: 重命名仓库

1. 进入 GitHub 仓库页面
2. 点击 "Settings"（设置）
3. 在 "Repository name" 中输入：`你的GitHub用户名.github.io`
   - 例如：如果你的用户名是 `zhangsan`，则输入 `zhangsan.github.io`
4. 点击 "Rename" 确认

#### 步骤 2: 启用 GitHub Pages

1. 在 Settings 页面，滚动到 "Pages" 部分（在左侧菜单中）
2. 在 "Source" 下拉菜单中选择：
   - Branch: `main` (或 `master`，取决于你的主分支名称)
   - Folder: `/ (root)`
3. 点击 "Save"

#### 步骤 3: 等待部署

- GitHub 会自动构建和部署你的网站
- 通常需要 1-5 分钟
- 你会在页面顶部看到一个绿色的提示："Your site is published at https://你的用户名.github.io"

#### 步骤 4: 访问你的网站

打开浏览器，访问：`https://你的用户名.github.io`

### 方法二：创建新仓库

如果你想从零开始：

#### 步骤 1: 创建新仓库

1. 登录 GitHub
2. 点击右上角的 "+" → "New repository"
3. 仓库名称**必须**是：`你的用户名.github.io`
4. 选择 "Public"（公开）
5. 不要勾选 "Initialize this repository with a README"
6. 点击 "Create repository"

#### 步骤 2: 上传文件

**选项 A: 使用 Git 命令行**

```bash
# 1. 进入你的模板文件夹
cd /path/to/your/template

# 2. 初始化 Git 仓库（如果还没有）
git init

# 3. 添加所有文件
git add .

# 4. 提交
git commit -m "Initial commit: Personal homepage"

# 5. 添加远程仓库
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git

# 6. 推送到 GitHub
git branch -M main
git push -u origin main
```

**选项 B: 使用 GitHub 网页上传**

1. 在新创建的仓库页面，点击 "uploading an existing file"
2. 将所有文件拖拽到上传区域
3. 等待上传完成
4. 点击 "Commit changes"

#### 步骤 3: GitHub Pages 会自动启用

由于仓库名称是 `用户名.github.io` 格式，GitHub Pages 会自动启用。

#### 步骤 4: 访问网站

等待 1-5 分钟后，访问：`https://你的用户名.github.io`

## 🔧 常见问题解决

### 问题 1: 网站显示 404 错误

**可能原因：**
- GitHub Pages 还在构建中（等待几分钟）
- 仓库名称不正确（必须是 `用户名.github.io`）
- GitHub Pages 未启用

**解决方法：**
1. 检查仓库名称是否正确
2. 进入 Settings → Pages 确认已启用
3. 等待 5-10 分钟再试

### 问题 2: 网站样式错误或图片不显示

**可能原因：**
- 文件路径不正确
- CSS/JS 文件缺失

**解决方法：**
1. 确保所有文件都已上传
2. 检查 HTML 中的文件路径（应该使用相对路径，如 `./css/style.css`）
3. 打开浏览器开发者工具（F12）查看错误信息

### 问题 3: 更新后网站没有变化

**可能原因：**
- 浏览器缓存
- GitHub Pages 更新延迟

**解决方法：**
1. 按 `Ctrl + F5`（Windows）或 `Cmd + Shift + R`（Mac）强制刷新
2. 清除浏览器缓存
3. 等待几分钟让 GitHub Pages 完成部署

### 问题 4: 最后更新时间不显示

**可能原因：**
- GitHub API 用户名或仓库名未更新

**解决方法：**
1. 打开 `index.html`
2. 找到第 72-95 行的脚本
3. 确保替换了：
   - `your-username.github.io` → 你的仓库名
   - `your-github-username` → 你的 GitHub 用户名

## 📝 更新网站内容

### 方法 1: 在 GitHub 网页上直接编辑

1. 进入你的仓库
2. 点击要编辑的文件
3. 点击右上角的铅笔图标（编辑）
4. 修改内容
5. 滚动到底部，点击 "Commit changes"

### 方法 2: 使用 Git 命令行

```bash
# 1. 修改文件

# 2. 添加更改
git add .

# 3. 提交
git commit -m "更新个人信息"

# 4. 推送到 GitHub
git push
```

## 🎨 自定义域名（可选）

如果你有自己的域名（如 `www.yourname.com`），可以将它绑定到 GitHub Pages：

1. 在仓库根目录创建一个名为 `CNAME` 的文件
2. 在文件中写入你的域名（例如：`www.yourname.com`）
3. 在你的域名提供商处配置 DNS：
   - 添加 CNAME 记录，指向 `你的用户名.github.io`
4. 等待 DNS 生效（可能需要几小时）

详细教程：https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## 📊 查看网站访问统计

你可以使用以下免费工具来跟踪网站访问量：

1. **Google Analytics**
   - 访问：https://analytics.google.com
   - 创建账户并获取跟踪代码
   - 将代码添加到每个 HTML 文件的 `<head>` 部分

2. **简单的访客计数器**
   - 可以使用第三方服务如 hits.sh 或 visitor-badge

## 🔒 安全建议

1. ❌ **不要**在网站上公开敏感信息（如完整的手机号码、家庭地址等）
2. ❌ **不要**上传私密文件到公开仓库
3. ✅ 使用邮箱时写成 `name (at) domain.com` 格式，避免垃圾邮件
4. ✅ 定期检查仓库，确保没有误传的敏感文件

## 📱 移动端优化

这个模板已经使用了响应式设计（Bootstrap），在移动设备上也能很好地显示。

你可以：
1. 在手机浏览器中打开网站测试
2. 使用浏览器开发者工具的移动设备模拟器测试

## 🆘 获取帮助

如果遇到问题：

1. **查看 GitHub Pages 文档**
   - https://docs.github.com/en/pages

2. **检查部署状态**
   - 进入仓库的 "Actions" 标签查看部署日志

3. **浏览器开发者工具**
   - 按 F12 打开
   - 查看 Console 标签中的错误信息

4. **GitHub 社区**
   - https://github.community/

## ✅ 部署检查清单

在宣布你的网站上线之前，请检查：

- [ ] 所有页面都能正常访问
- [ ] 个人照片正确显示
- [ ] 社交媒体链接都是正确的
- [ ] 没有示例内容或模板文字
- [ ] 导航栏链接都能工作
- [ ] 在手机上测试过显示效果
- [ ] 所有 "你的名字" 占位符都已替换
- [ ] GitHub 用户名和仓库名都已更新

## 🎉 完成！

恭喜你！你的个人主页现在已经在互联网上了！

别忘了：
- 在社交媒体上分享你的网站链接
- 把链接添加到你的 LinkedIn、简历等地方
- 定期更新内容保持网站活跃

---

**有任何问题？** 随时查看 README.md 或搜索相关教程。祝你使用愉快！ 🚀
