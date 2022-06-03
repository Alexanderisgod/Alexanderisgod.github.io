---
title: Setup Blog
date: 2022-06-03 16:07:50
categories: 
- hexo
tags: 
- Next
---
#### Hexo set up
1. Github blog setup reference: [How to setup blog on github?](https://adsuper.github.io/2017/03/19/%E5%9F%BA%E4%BA%8EHexo-Github-%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2%E7%AC%94%E8%AE%B0-1/)

2. hexo使用theme出现“ % extends ‘_layout.swig‘ % % import ‘_macro/post.swig‘ as post_template %“问题

> 原因是hexo在5.0之后把swig给删除了需要自己手动安装
>
> npm i hexo-renderer-swig

<!--more-->
3. 问题

> FATAL {
>   err: Template render error: (unknown path)
>     Error: template names must be a string: undefined
>       at Object._prettifyError (E:\blog\node_modules\nunjucks\src\lib.js:36:11)

数学公式中’#'的错误插入导致了整个Hexo博客的崩溃，把这行公式用图片替代，问题就解决啦

类似的，两层花括号嵌套也会引发错误，注意避免。[参考链接](https://muzing.top/posts/6605/)