# Dan's Blog — Hugo + Liva-Hugo Theme

A professional personal blog and portfolio powered by [Hugo](https://gohugo.io/) and the [Liva-Hugo](https://github.com/gethugothemes/liva-hugo) theme. Showcases projects, Medium articles, and professional links for a Semiconductor Failure Engineer & Full-Stack Developer.

---

## 🚀 Features
- **Modern Hugo static site** with Liva-Hugo theme
- **Customizable portfolio**: GitHub projects, Medium posts, LeetCode, LinkedIn, and more
- **Contact form**: Sends email to your address via mailto
- **Google Analytics 4** integration
- **Production-ready**: Clean URLs, SEO, and responsive design
- **Python helper scripts** for content and build management

---

## 🛠️ Setup

### 1. Prerequisites
- [Hugo](https://gohugo.io/getting-started/installing/) (extended version recommended)
- [Python 3](https://www.python.org/downloads/)
- [Git](https://git-scm.com/)

### 2. Clone the Repository
```bash
git clone https://github.com/1daniel3333/blog_cursor.git
cd blog_cursor
```

### 3. Install Python Dependencies
```bash
pip install Pillow PyYAML
```

### 4. Run the Setup Script (Optional)
To create a new Hugo site with the Liva-Hugo theme:
```bash
python setup_liva_hugo.py
```

---

## 📝 Customization

### Content & Portfolio
- **Blog posts**: `danblog/content/english/blog/`
- **About page**: `danblog/content/english/about/_index.md`
- **Contact page**: `danblog/content/english/contact/_index.md`
- **Portfolio/projects**: `danblog/data/projects.yml`
- **Images**: Place in `danblog/static/images/projects/` and `danblog/static/images/posts/`

### Social Links
Edit `danblog/hugo.toml` under `[[params.social]]` for GitHub, LinkedIn, Medium, LeetCode, etc.

### Site Info
Edit `danblog/hugo.toml` and `danblog/config/_default/hugo.toml` for:
- Site title, description, author
- Copyright
- Base URL (for deployment)

### Google Analytics
Already integrated. To change the tracking ID, edit `danblog/themes/liva-hugo/layouts/partials/head.html`.

---

## 📦 Build & Deploy

### 1. Build for Production
```bash
python build_for_production.py
```
Or manually:
```bash
cd danblog
hugo --minify
```

### 2. Deploy to GitHub Pages
- Push the contents of `danblog/public/` to your `gh-pages` branch or your repository root (for user/organization pages)
- Ensure `baseURL` in `danblog/config/_default/hugo.toml` matches your GitHub Pages URL
- Enable GitHub Pages in your repository settings

### 3. Your Site Will Be Live At
```
https://1daniel3333.github.io/about/
```

---

## 🐍 Python Helper Scripts
- `setup_liva_hugo.py`: One-click Hugo + theme setup
- `customize_blog.py`: Create new blog posts and get customization tips
- `update_projects.py`: Manage your portfolio and professional links
- `generate_logo_favicon.py`: Generate a tech-themed logo and favicon
- `build_for_production.py`: Clean build for deployment

---

## 📄 License
This project uses the [Liva-Hugo theme](https://github.com/gethugothemes/liva-hugo) (MIT License) and is open for personal and professional use.

---

## ✨ Credits
- [Liva-Hugo Theme](https://github.com/gethugothemes/liva-hugo)
- [Hugo](https://gohugo.io/)
- [Themify Icons](https://themify.me/themify-icons)

---

**Made with ❤️ by Dan** 
