# roslaan-blog

A high-performance, premium Brutalist blog built with **Hugo** and managed via **Decap CMS**.

---

## 🚀 Local Development & Testing

To test the site locally, you can use the bundled `hugo` binary.

### 1. Start the Hugo Server
Run the following command in your terminal:

```bash
./hugo server -D
```
*The `-D` flag includes draft posts.*

### 2. View the Site
Open your browser and navigate to:
[http://localhost:1313](http://localhost:1313)

### 3. Test Decap CMS
To access the CMS dashboard locally (for UI testing):
[http://localhost:1313/admin/](http://localhost:1313/admin/)

> [!NOTE]
> Changes made in the local CMS will not be saved to GitHub unless you set up a local proxy (like `decap-server`). For most edits, it's easier to use the live CMS at `https://roslaan.github.io/admin/`.

---

## 📝 Writing a New Post

### Via Decap CMS (Recommended)
1. Go to your live site's admin panel: `https://roslaan.github.io/admin/`
2. Log in with your GitHub account.
3. Click "New Post" and start writing.

### Via Command Line
Create a new markdown file in `content/posts/`:

```bash
./hugo new posts/your-post-title.md
```

Each post should have this front matter:

```yaml
---
title: "Your Post Title"
date: 2026-03-25T18:30:00Z
summary: "A brief teaser for the article list."
draft: false
---

Your content here in Markdown...
```

---

## 🛠 Project Structure

```
roslaan-blog/
├── content/             ← your articles go here (Markdown)
├── static/              ← images, admin config, etc.
├── themes/
│   └── essence/         ← bespoke Brutalist theme
├── hugo.toml            ← main site configuration
├── hugo                 ← bundled Hugo binary
└── README.md
```

---

## 🚢 Deployment

The site is automatically deployed to **GitHub Pages** whenever you push to the `main` branch via GitHub Actions.


docker run -d \
  -p 8082:8080 \
  -p 50000:50000 \
  --name jenkins \
  -v jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  --restart=on-failure \
  jenkins/jenkins:lts-jdk21


  docker run -d -v jenkins_home:/var/jenkins_home --name jenkins -p 8082:8080 -p 50000:50000 --restart=on-failure jenkins/jenkins:lts-jdk21