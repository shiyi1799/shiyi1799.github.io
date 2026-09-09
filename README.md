# ShiYi的随笔

记录生活、技术与思考的个人博客，基于 [Jekyll](https://jekyllrb.com/) 搭建，托管在 [GitHub Pages](https://pages.github.com/)。

在线访问：<https://shiyi1799.github.io/>

## 目录结构

```
.
├── _config.yml            # 站点配置（标题、描述、链接格式等）
├── _layouts/              # 布局模板
│   ├── default.html       # 全站外壳
│   └── post.html          # 文章页模板
├── _posts/                # 文章（Markdown）
├── assets/css/style.css   # 主题样式
├── index.html             # 首页（自动列出所有文章）
├── about.md               # 关于页
├── feed.xml               # RSS 订阅源
└── 404.html               # 404 页面
```

## 如何写一篇新文章

在 `_posts/` 目录下新建一个 Markdown 文件，**文件名必须以日期开头**，例如：

```
_posts/2026-09-09-my-new-post.md
```

文件顶部加上 front matter：

```yaml
---
layout: post
title: "文章标题"
date: 2026-09-09 12:00:00 +0800
tags: [技术]
excerpt: "一句话摘要，会显示在首页文章列表里。"
---

正文用 Markdown 写在这里……
```

commit 并 push 到 `main` 分支，GitHub Actions 会自动构建并发布，几分钟后就能在网站上看到。

## 本地预览（可选）

需要先安装 Ruby 和 Jekyll，然后：

```bash
gem install jekyll bundler
bundle exec jekyll serve
```

浏览器打开 <http://localhost:4000> 即可预览。

## 联系

邮箱：shiyi1799@126.com
