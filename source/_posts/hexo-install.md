---
title: 用homebrew安裝Hexo
date: 2018-03-14 23:25:46
categories:
- Hexo
tags: Hexo
---

* 安裝hexo:
    * 安裝node和npm：`brew install node`
    * 使用npm安裝Hexo `npm install -g hexo-cli`
    * 初始化blog： `hexo init blog`
    * 檢測安裝是否成功：`hexo new test_my_site`, `hexo g`, `hexo s`
    * 修改_config.yml的deploy部分：
    ```
    # Deployment
    ## Docs: https://hexo.io/docs/deployment.html
    deploy:
    type: git
    repo: https://github.com/testman007/testman007.github.io.git
    branch: master
    ```
    * 安裝Git部署插件：`npm install hexo-deployer-git --save`
    * 輸入部署指令：`hexo clean`, `hexo g`, `hexo d`
    * 網址https://testman007.github.io 即完成。

* 加入 Google Analytics
    * ./themes/landscape/_config.yml
    * 找到 google_analytics：後，把ID貼上。
    * 追蹤 ID：UA-115652689-1

* 安裝主題 hexo-theme-hueman：
    * github: https://github.com/ppoffice/hexo-theme-hueman

*手動新增sitemap:    
    *使用網站XML-Sitemaps.com產生sitemap.xml，上傳到GitHub/blog的根目錄，到Google Search Console新增sitemap的url，結束。