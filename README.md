
# 🛠️ Personal Hugo Website with Auto Update via GitHub Actions

This project is my personal static website built using [Hugo](https://gohugo.io/) and hosted on GitHub Pages. It supports **automated content updates** (e.g. fetching subscription data) using scheduled [GitHub Actions](https://docs.github.com/en/actions).

Read the full walkthrough here 👉 [Medium Article Chinese](https://medium.com/@p123456dan.mse99/%E7%94%A8-hugo-github-action-%E6%89%93%E9%80%A0%E8%87%AA%E5%8B%95%E6%9B%B4%E6%96%B0%E7%9A%84%E5%80%8B%E4%BA%BA%E9%9D%9C%E6%85%8B%E7%B6%B2%E7%AB%99-1b0c65f3f5ff)/[Medium Article English](https://medium.com/@p123456dan.mse99/build-an-auto-updating-personal-static-website-with-hugo-github-actions-bcdcd6e8db44)

---

## 🧱 Tech Stack

| Tool | Description |
|------|-------------|
| [Cursor](https://www.cursor.sh/) | AI-friendly IDE for developing Hugo content |
| [Hugo](https://gohugo.io/) | Static Site Generator |
| [GitHub Pages](https://pages.github.com/) | Hosting platform for static sites |
| [GitHub Actions](https://docs.github.com/en/actions) | CI/CD and cron automation |
| Python | Used to dynamically update content via scraping/API |

---

## 🗂️ Project Structure

```
📁 .github/workflows/      # GitHub Actions workflow files
📁 content/                # Blog posts and page content
📁 static/                 # Static files (e.g., images, favicon)
📁 themes/                 # Hugo theme (customized from upstream)
📁 public/                 # (auto-generated) Final HTML site content
📄 config.toml            # Hugo config file
```

---

## 🔄 Automated Update Flow

1. Python script in a **private repo** collects external data (e.g., subscriptions, feeds).
2. GitHub Actions (via cron) runs the script.
3. Output is committed & pushed to this repo.
4. Hugo rebuilds the site content and auto-deploys via GitHub Pages.

See diagram:

![flowchart](./assets/architecture.png)

---

## 🚀 Getting Started

### 1. Install Hugo

```bash
brew install hugo
```

### 2. Clone Repository

```bash
git clone https://github.com/1daniel3333/1daniel3333.github.io.git
cd 1daniel3333.github.io
```

### 3. Run Hugo Server Locally

```bash
hugo server -D
```

### 4. Customize Theme

Modify theme files under `/themes/` or fetch a new one:

```bash
hugo new site mysite
cd mysite
git init
git submodule add https://github.com/theme-repo themes/themename
```

---

## ⚙️ GitHub Actions Setup

- GitHub Actions defined under `.github/workflows/`.
- A `cron` schedule is used to auto-fetch and regenerate content.
- Output is pushed into `main` branch (`public/` folder).

```yaml
on:
  schedule:
    - cron: '0 2 * * *'  # every day at 02:00 UTC
```

---

## 🙏 Acknowledgements

- [kucw's Hugo/GitHub Pages guide](https://kucw.io/blog/2021/1/from-medium-to-github/)
- [zhgchg's GitHub Actions article](https://dev.zhgchg.li/ci-cd-%E5%AF%A6%E6%88%B0%E6%8C%87%E5%8D%97-%E4%BA%8C-github-actions-%E8%88%87-self-hosted-runner-%E4%BD%BF%E7%94%A8%E8%88%87%E5%BB%BA%E7%BD%AE%E5%A4%A7%E5%85%A8-404bd5c70040)

---

## 📬 Contact

Feel free to reach out via Medium or GitHub issues if you have questions!
