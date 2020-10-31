---
title: hexo
date: 2010-10-31 14:29:35
keywords:
description:
categories:
tags:
---

[官方文档](https://hexo.io/zh-cn/docs/)

## 建站

```bash
# 安装 hexo 环境
npm i hexo
# 初始化项目
hexo init test
# 新建模板文章
# 参考scaffolds下模板，默认post
hexo new post hello-world
```

## 配置命令

`package.json`

```json
{
   "scripts": {
    "dev": "hexo s --port 3030",
    "serve": "hexo clean && hexo g && hexo s --port 3030",
    "build": "hexo clean && hexo g && hexo d"
  }
}
```

## 主题

```bash
npm install hexo-theme-next
```

`_config.yml`

```yml
theme: next
```

`node_modules/hexo-theme-next/_config.yml`

```yml
scheme: Gemini
```

## 菜单

`node_modules/hexo-theme-next/_config.yml`

```yml
# 需要按照url添加相应文件
menu:
  home: / || fa fa-home
  about: /about/me || fa fa-user
  tags: /tags/ || fa fa-tags
  categories: /categories/ || fa fa-th
  archives: /archives/ || fa fa-archive
  schedule: /schedule/ || fa fa-calendar
  # sitemap: /sitemap.xml || fa fa-sitemap
  commonweal: /404/ || fa fa-heartbeat
```

## valine

- [登录leancloud](https://leancloud.cn/dashboard/applist.html#/apps)
- appId+appKey: 应用-设置-应用keys
- 用户评论数据: 存储-结构化数据-comment

```yml
valine:
  enable: true
  appid: ObXHInAOnvOfLg9zzIm3bzEL-gzGzoHsz # Your leancloud application appid
  appkey: np5CE5m6AmCsA3oDQozGab1R # Your leancloud application appkey
```


## 模板语法使用讲解

### jsfiddle

1. [创建jsfiddle账号](https://jsfiddle.net/)
2. [进入jsfiddle个人管理界面](https://jsfiddle.net/user/fiddles/all/)
3. new fiddle
4. save 生成的链接填入下方, 如`1572413095/sytxg7u0/1/ `
  ```md
  {% jsfiddle 1572413095/sytxg7u0/1/  js,html,css,result  dark %}
  ```

{% jsfiddle 1572413095/sytxg7u0/1/  js,html,css,result  dark %}

### gist

1. [打开网址](http://gist.github.com)
2. 填写你的代码段，文件名，create secret/public git 
3. view your gists
4. 找到你的代码段打开，从url中获取你的gist_id
  ```md
  {% gist 0a986e502066914627d2bdec85f5ec7d regexp.exec.js %}
  ```

{% gist 0a986e502066914627d2bdec85f5ec7d regexp.exec.js %}

### iframe

```md
{% iframe https://lx0427.github.io/vuepress/ 100% 400 %}
```

{% iframe https://lx0427.github.io/vuepress/ 100% 400 %}


### link

```md
{% link 百度一下 http://www.baidu.com [external] [超链接] %}
```

{% link 百度一下 http://www.baidu.com [external] [超链接] %}

### youtube

```md
{% youtube lJIrF4YjHfQ %}
```

<!-- {% youtube lJIrF4YjHfQ %} -->

### vimeo

```md
{% vimeo 180916725 %}
```

<!-- {% vimeo 180916725 %} -->

### image

<!-- {% asset_img 01.png This is an example image %}  -->





