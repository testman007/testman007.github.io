---
title: hexo-在多台電腦同步使用
date: 2018-03-27 15:22:49
categories:
- hexo
tags:
- hexo
---

在擁有多台電腦的場合，會希望可以在每台電腦上都可以更新hexo，所以研究一下怎麼同步，基本上就是利用github去同步source的內容。

步驟：

1. 在blog的目錄資料夾，初始化git，並設定git remote:
```
git init
git remote add origin https://github.com/xxx/xxx.githubio 
```
xxx是你的repo地址

2. 接著，下指令創建 branch，然後 commit / push:
```
git checkout -b remote-source
git add .
git commit -m "Add new branch remote-source"
git push -u origin remote-source
```

3. 大功告成，在另一台電腦，把project整個clone下來，再checkout到remote-source分支，然後執行npm install就可以了，如果有安裝主題也記得要用npm去安裝:

```
git clone xxxxxxxx
git checkout remote-source
npm install
```

4. branch 的檔案內容如下：

![](/img/hexo/github.jpg)




