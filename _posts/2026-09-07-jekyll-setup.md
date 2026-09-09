---
layout: post
title: "从零搭建 Jekyll 博客的完整笔记"
date: 2026-09-07 20:00:00 +0800
tags: [技术]
excerpt: "记录用 Jekyll + GitHub Pages 搭建个人博客的完整流程：目录结构、配置、布局与文章发布。"
---

把搭这个博客的过程完整记录下来，既是给自己备忘，也希望能帮到有同样需求的人。

## 目录结构

一个最小可用的 Jekyll 博客长这样：

```
.
├── _config.yml        # 站点配置
├── _layouts/          # 布局模板
│   ├── default.html   # 全站外壳（导航、页脚）
│   └── post.html      # 文章页模板
├── _posts/            # 文章（Markdown）
├── assets/css/        # 样式
├── index.html         # 首页
└── feed.xml           # RSS
```

## 核心概念

Jekyll 里最重要的两个概念：

- **Layout**：页面的「骨架」，通过 `layout: xxx` 指定，内容用 `{% raw %}{{ content }}{% endraw %}` 注入
- **Post**：放在 `_posts/` 下、文件名以日期开头的 Markdown 文件，会自动按时间排序

## 写一篇文章

在 `_posts/` 下新建 `2026-09-08-hello-world.md`，顶部写 front matter：

```yaml
---
layout: post
title: "文章标题"
date: 2026-09-08 12:00:00 +0800
tags: [技术]
---
正文写在这里……
```

commit 并 push 到 GitHub，几分钟后文章就自动出现在网站上了，非常省心。
