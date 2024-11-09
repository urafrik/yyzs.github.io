---
permalink: /
title: "Academic Pages 是一个适用于学术个人网站的GitHub Pages模板，随时可供复刻"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

这是一个由 [Academic Pages 模板](https://github.com/academicpages/academicpages.github.io)支持、在 GitHub Pages 上托管的网站的主页。[GitHub Pages](https://pages.github.com) 是一项免费的服务，网站内容可以通过存储在 GitHub 仓库中的代码和数据自动更新。该模板基于 Michael Rose 创建的 [Minimal Mistakes Jekyll 主题](https://mmistakes.github.io/minimal-mistakes/)复刻，并扩展了适用于学术内容的支持，如论文、演讲、教学、作品集、博客文章和动态生成的简历。你可以立即复刻 [这个模板](https://github.com/academicpages/academicpages.github.io)，修改配置和 Markdown 文件，添加自己的 PDF 和其他内容，免费拥有自己的网站，无广告！

一个数据驱动的个人网站
======
与许多其他基于 Jekyll 的 GitHub Pages 模板一样，Academic Pages 将网站的内容与形式分离。网站的内容和元数据存储在结构化的 Markdown 文件中，而其他文件则构成主题，指定如何将内容和元数据转换为 HTML 页面。你可以将这些不同的 Markdown (.md)、YAML (.yml)、HTML 和 CSS 文件存储在公开的 GitHub 仓库中。每次你提交并推送更新至仓库时，[GitHub Pages](https://pages.github.com/) 服务会基于这些文件创建静态 HTML 页面，并免费托管在 GitHub 服务器上。

许多动态内容管理系统（如 WordPress）的功能可以通过这种方式实现，所需计算资源更少，也不易受到黑客攻击或DDoS的影响。你还可以在不修改网站内容的情况下任意调整主题设计。如果你在 Jekyll/HTML/CSS 上遇到无法修复的问题，描述你的演讲、论文等的 Markdown 文件依然是安全的。你可以回滚更改，甚至删除仓库并重新开始——只要保存好这些 Markdown 文件！最后，你也可以编写脚本来处理站点上的结构化数据，例如[这个脚本](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb)，用于分析演讲页面中的元数据并展示你演讲过的地点地图（例如[此地图](https://academicpages.github.io/talkmap.html)）。

开始使用
======
1. 注册一个 GitHub 账户（如果还没有的话）并确认邮箱（必需）
1. 点击页面右上角的“Use this template”按钮复刻 [此模板](https://github.com/academicpages/academicpages.github.io)
1. 进入仓库的设置页面（在“Code”选项卡右侧）。将仓库重命名为“[你的 GitHub 用户名].github.io”，这将成为你网站的 URL
1. 设置全站配置并创建内容和元数据（详见下文——也可参考 [这组更改](http://archive.is/3TPas)，展示了如何为用户名“getorg-testacct”的用户设置 [示例站点](https://getorg-testacct.github.io)）
1. 上传任何文件（如 PDF、.zip 文件等）到 files/ 目录。这些文件会显示在 https://[你的 GitHub 用户名].github.io/files/example.pdf
1. 前往仓库设置页面，检查“GitHub Pages”部分的状态

全站配置
------
网站的主要配置文件位于根目录的 [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml) 中，定义了侧边栏和其他站点功能的内容。你需要用自己的信息和 GitHub 仓库的内容替换默认变量。顶级菜单的配置文件位于 [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml)。例如，如果你没有作品集或博客文章，可以从 navigation.yml 文件中移除这些项目以从头部导航中删除它们。

创建内容和元数据
------
站点内容使用独立的 Markdown 文件存储，每种内容类型有一个目录，如 _publications、_talks、_posts、_teaching 或 _pages。例如，每个演讲对应 [_talks 目录](https://github.com/academicpages/academicpages.github.io/tree/master/_talks)中的一个 Markdown 文件。每个 Markdown 文件顶部包含 YAML 格式的结构化数据，主题会解析这些数据生成各种页面。演讲的结构化数据用于生成 [演讲页面](https://academicpages.github.io/talks)上的列表，每个具体演讲的 [单独页面](https://academicpages.github.io/talks/2012-03-01-talk-1)，[简历页面](https://academicpages.github.io/cv)的演讲部分，以及[演讲地点地图](https://academicpages.github.io/talkmap.html)（如果运行 [python 文件](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py)或 [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb)）。

**Markdown 文件生成器**

该仓库包含一组 [Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator)，可将包含演讲或展示的结构化数据的 CSV 文件转换为适用于 Academic Pages 模板的 Markdown 文件。示例 CSV 文件是我用于创建个人网站 stuartgeiger.com 的数据。我通常会将我的出版物和演讲记录在电子表格中，然后运行 notebook 中的代码生成 Markdown 文件，接着提交并推送至 GitHub 仓库。

如何编辑站点的 GitHub 仓库
------
许多人使用 git 客户端在本地计算机上创建文件，然后推送到 GitHub 的服务器。如果不熟悉 git，可以直接在 github.com 界面上编辑配置和 Markdown 文件。进入一个文件（例如 [这个文件](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md)），点击右上角的铅笔图标（在“Raw | Blame | History”按钮右侧）。可以点击铅笔图标右侧的垃圾桶图标删除文件。也可以在目录中点击“Create new file”或“Upload files”按钮创建或上传新文件。

示例：编辑演讲的 Markdown 文件
![编辑演讲的 Markdown 文件](/images/editing-talk.png)

更多信息
------
有关 Academic Pages 配置的更多信息，请参考 [指南](https://academicpages.github.io/markdown/)、[不断增长的 Wiki](https://github.com/academicpages/academicpages.github.io/wiki)，或者在 [GitHub 上提问](https://github.com/academicpages/academicpages.github.io/discussions)。[Minimal Mistakes 主题的指南](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)（该主题派生自此主题）也可能有帮助。
