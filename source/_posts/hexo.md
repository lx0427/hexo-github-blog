---
title: hexo
date: 2010-10-31 14:29:35
keywords:
description:
categories:
tags:
  - hexo
  - hexo-theme-next
  - jsfiddle
  - gist
  - valine
  - github-page
---

[官方文档](https://hexo.io/zh-cn/docs/)

## 建站

```bash
# 安装 hexo 环境
npm i hexo
# 初始化项目
hexo init test
# 初始化git仓库，git clone
# 拷贝test中文件到项目文件夹中
npm install
# 启动项目，看到hello-world
npm run server 
```

## 主题&语言

```bash
# copy to themes/hexo-theme-next
npm install hexo-theme-next
```

`_config.yml`

```yml
theme: hexo-theme-next
# 语言
language: zh-CN
```

## 主题功能

`hexo-theme-next/_config.yml`

```yml
# 主题风格
scheme: Gemini

# 需要按照url添加相应文件
menu:
  home: / || fa fa-home
  about: /about/ || fa fa-user
  tags: /tags/ || fa fa-tags
  categories: /categories/ || fa fa-th

# 打赏
reward_settings:
  # If true, a donate button will be displayed in every article by default.
  enable: true
  # animation: true
  comment: Buy me a coffee

reward:
  wechatpay: /images/wechatpay.jpg # 替换主题images中的图片
  alipay: /images/alipay.jpg
  #paypal: /images/paypal.png
  #bitcoin: /images/bitcoin.png

# 复制代码块
codeblock:
  copy_button:
    enable: false
  # Available values: default | flat | mac
  style:
```

### tags

```bash
hexo new page tags
# tags/index.md 中添加 type: "tags"
# 暂无标签
```

### categories

```bash
hexo new page categories
# categories/index.md 中添加 type: "categories"
# 暂无分类
```

## 站内搜索

```bash
npm install hexo-generator-searchdb
```

`_config.yml`

```yml
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```

`hexo-theme-next/_config.yml`

```yml
local_search:
  enable: true
```

## valine

- [登录leancloud](https://leancloud.cn/dashboard/applist.html#/apps)
- appId+appKey: 应用-设置-应用keys
- 用户评论数据: 存储-结构化数据-comment
- serverURLs: [访问官网](https://valine.js.org/)控制台network查看Comment接口域名

```yml
valine:
  enable: true
  appId: XkDAbvFcnXugtkXyVCUF3Bcb-gzGzoHsz # Your leancloud application appid
  appKey: UMru31u3af0ELnibVJqnk93C # Your leancloud application appkey
  serverURLs: https://avoscloud.com # When the custom domain name is enabled, fill it in here
```

## 发布到github-page

```bash
npm install hexo-deployer-git
```

`_config.yml`

```yml
deploy:
  type: git
  repo: https://github.com/lx0427/lx0427.github.io.git
  branch: gh-pages
```

## 配置命令

`package.json`

```json
{
  "scripts": {
    "dev": "hexo server --port 3030",
    "serve": "hexo clean && hexo generate && hexo server --port 3030",
    "build": "hexo clean && hexo generate && hexo deploy"
  },
}
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





