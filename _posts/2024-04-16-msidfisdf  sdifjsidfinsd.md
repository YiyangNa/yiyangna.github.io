---
layout: post  # 指定使用哪个布局文件 (通常是 post)
title: "我的第一篇文章" # 文章的标题
date: 2023-04-16 10:30:00 +0800 # 可选，但推荐，会覆盖文件名中的日期，注意时区
categories: [技术, 博客] # 可选，文章分类
tags: [Jekyll, Chirpy] # 可选，文章标签
# 其他你需要的元数据...
---

太棒了！既然你已经成功地将代码克隆到 Docker Volume 并且 Dev Container 环境应该已经在 VS Code 中运行起来了，接下来的步骤就是**启动本地预览服务器，看看你的网站效果，然后开始配置和添加内容**。

参照我们之前看的 Chirpy 主题文档，你现在应该执行以下步骤：

1. **打开 VS Code 的集成终端：**

   - 确保你的 VS Code 左下角仍然显示你处于 Dev Container 环境中 (类似 Dev Container: Jekyll 或你设置的名称)。
   - 点击 VS Code 顶部菜单栏的 Terminal (终端) -> New Terminal (新建终端)。这会在 VS Code 底部打开一个终端面板，并且这个终端是**在容器内部运行的**，而不是在你的 Windows 系统里。

2. **启动 Jekyll 本地服务器：**

   - 在打开的 VS Code 终端中，输入以下命令，然后按 Enter：

     ```
           bundle exec jekyll s
         
     ```

   - **解释：**

     - bundle exec: 确保命令使用的是项目 Gemfile 里定义的特定版本 Jekyll 和插件。
     - jekyll s (是 serve 的缩写): 告诉 Jekyll 构建你的网站（把 Markdown 文件等转换成 HTML）并在你的本地机器上启动一个 Web 服务器。

3. **等待服务器启动并预览：**

   - 终端会输出一些构建信息。如果一切顺利，最后你会看到类似这样的信息：

     ```
           Server address: http://127.0.0.1:4000/
     Server running... press ctrl-c to stop.
     ```    *   **VS Code 可能会自动弹出一个提示**，询问你是否要在浏览器中打开转发的端口。你可以直接点击 "Open in Browser"。
         
     ```

     IGNORE_WHEN_COPYING_START

      content_copy  download 

      Use code [with caution](https://support.google.com/legal/answer/13505487).

     IGNORE_WHEN_COPYING_END

   - **或者**，你可以手动打开你的 Windows 浏览器（如 Edge, Chrome, Firefox），在地址栏输入 http://127.0.0.1:4000 (或者终端输出的确切地址)，然后访问。

   - **你应该就能看到你的 Chirpy 主题网站的初始样子了！**

4. **开始探索和配置：**

   - **浏览网站：** 点击看看默认的页面和布局。
   - **查看文件结构：** 在 VS Code 左侧的文件浏览器中，熟悉一下项目的目录结构，特别是：
     - _config.yml: 主要的站点配置文件。
     - _posts: 存放你的博客文章 (Markdown 文件)。
     - _data: 存放数据文件，比如 contact.yml 社交链接。
     - assets: 存放 CSS、JavaScript、图片等静态资源。
     - pages 或根目录下的 .md 文件：可能包含 "About" 等独立页面。
   - **尝试修改 _config.yml:** 打开这个文件，尝试修改 title (网站标题) 或 tagline (标语)。
     - **重要：** 修改 _config.yml 后，你需要**停止** Jekyll 服务器 (回到 VS Code 终端，按 Ctrl + C)，然后**重新运行** bundle exec jekyll s 命令，更改才会生效。
   - **尝试修改其他文件：** 试着修改一下 _posts 目录下的示例文章，或者 index.md (首页) 的内容。保存文件后，Jekyll 服务器通常会自动检测到变化并重新构建。你只需要**刷新浏览器**就能看到更新（不需要重启服务器，除非改了 _config.yml）。

5. **停止服务器：**

   - 当你暂时不需要预览时，可以回到 VS Code 终端，按 Ctrl + C 来停止 Jekyll 服务器。

**总结一下你现在该做的：**

1. 在 **VS Code 终端**里运行 bundle exec jekyll s。
2. 在浏览器里访问 http://127.0.0.1:4000 查看你的网站。
3. 开始修改 _config.yml 和其他内容文件，熟悉 Jekyll 和 Chirpy 的工作方式。记住修改 _config.yml 需要重启服务器。

祝你玩得开心！开始打造你的专属网站吧！
