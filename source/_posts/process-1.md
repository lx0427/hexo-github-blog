---
title: process-1
date: 2019-01-08 16:35:32
keywords:
description:
categories:
tags:
---

## 流程图

### 模块语法

示例
```
st=>start: start:>https://lx0427.github.io/[blank]
e=>end: end
op=>operation: 操作
cond=>condition: 判断
sub=>subroutine: 子任务块
io=>inputoutput: I/O

st->op->cond
cond(no)->io->e
cond(yes)->sub->e
```
效果
```flow
st=>start: start:>https://lx0427.github.io/[blank]
e=>end: end
op=>operation: 操作
cond=>condition: 判断
sub=>subroutine: 子任务块
io=>inputoutput: I/O

st->op->cond
cond(no)->io->e
cond(yes)->sub->e
```


