---
title: Hexo+Github+git
date: 2020-04-05 19:45:12
tags: blog_site_built-up
---
## 配置Github和git
### 配置什么?
![配置什么](/public/blog-imgs/20040501_01.png) 

### 配置流程

### 解决contribution没有被记录的问题
* 原因[5]：
``` shell
	GitHub uses the email address set in your local Git configuration to associate commits 
	pushed from the command line with your GitHub account.
```
* 设置命令[5]：
``` shell
	git config user.email "email@example.com"
	git config user.name
```
* windows查看配置文件:
``` shell
全局配置文件
	cat ~/\.gitconfig
本地仓库配置文件
	在.git文件夹中
```


## 参考
1) https://juejin.im/post/5accc3c9f265da23870f2abc
2) https://github.com/firebase/firebase-tools/issues/486
3) https://git-scm.com/book/zh/v2/%E6%9C%8D%E5%8A%A1%E5%99%A8%E4%B8%8A%E7%9A%84-Git-%E7%94%9F%E6%88%90-SSH-%E5%85%AC%E9%92%A5#_generate_ssh_key
4) https://www.jianshu.com/p/802adf6aab52
5) https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address