# Alessio Borzì's Personal Homepage

This is a personal academic homepage based on a YAML configuration system with markdown content files.

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

### 3. Update Images

Replace the following images in `static/assets/img/`:
- `photo.png` - Your profile photo
- `background.png` - Background image for the top section

### 4. Update Links

Edit `index.html` to update footer links (lines 182-185):
- GitHub profile link
- License link

## 📁 Directory Structure

```
.
├── contents/           # Content files
│   ├── config.yml     # Configuration
│   ├── home.md        # Home section
│   ├── awards.md      # Awards section
│   ├── experience.md  # Experience section
│   └── publications.md # Publications section
├── static/            # Static assets
│   ├── assets/        # Images and favicon
│   ├── css/           # Stylesheets
│   └── js/            # JavaScript files
└── index.html         # Main HTML file
```

## 🌐 Deployment

This website is designed to be deployed on GitHub Pages. Once you push your changes to the repository, GitHub Pages will automatically build and deploy your website.

## 📝 License

This template is based on [Sen Li's academic homepage template](https://github.com/senli1073/senli1073.github.io).

## 👤 Author

**Alessio Borzì**
- Email: alessioborzi.math (at) gmail.com
- GitHub: [@AlessioBorzi](https://github.com/AlessioBorzi)
- Homepage: [alessioborzi.github.io](https://alessioborzi.github.io)
