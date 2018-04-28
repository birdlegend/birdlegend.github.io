---
title: github和hexo搭建博客教程集合
date: 2018-04-28 14:54:31
categories:
- github.io
tags:
- hexo
- github.io
---
#### [GitHub Pages + Hexo搭建博客](http://crazymilk.github.io/2015/12/28/GitHub-Pages-Hexo%E6%90%AD%E5%BB%BA%E5%8D%9A%E5%AE%A2/#more)


>当重装电脑之后，或者想在其他电脑上修改博客，可以使用下列步骤：  
使用git clone git@github.com:CrazyMilk/CrazyMilk.github.io.git拷贝仓库（默认分支为hexo）；
在本地新拷贝的CrazyMilk.github.io文件夹下通过Git bash依次执行下列指令：npm install hexo、npm install、npm install hexo-deployer-git（记得，不需要hexo init这条指令）。

  ​

#### [Hexo使用攻略-添加分类及标签](https://www.jianshu.com/p/e17711e44e00)

#### [Hexo之next主题设置首页不显示全文(只显示预览)](https://www.jianshu.com/p/393d067dba8d)
> 进入hexo博客项目的themes/next目录
用文本编辑器打开_config.yml文件
搜索"auto_excerpt",找到如下部分：
```
auto_excerpt:
  enable: false
  length: 150
```
把enable改为对应的false改为true，length改为0，然后hexo d -g，再进主页，问题就解决了！

