---
title: hexo搭建
date: 2020-08-14 02:21:03
tags:

---

## 安装Nodejs
node -v #查看node版本
npm -v #查看npm版本
npm install -g cnpm --registry=http://registry.npm.taobao.org #安装淘宝的cnpm 管理器
cnpm -v #查看cnpm版本
cnpm install -g hexo-cli #安装hexo框架
hexo -v #查看hexo版本
mkdir blog #创建blog目录
cd blog #进入blog目录
sudo hexo init #生成博客 初始化博客
hexo s #启动本地博客服务
http://localhost:4000/ #本地访问地址
hexo n "我的第一篇文章" #创建新的文章
#返回blog目录
hexo clean #清理
hexo g #生成
#Github创建一个新的仓库 YourGithubName.github.io
cnpm install --save hexo-deployer-git #在blog目录下安装git部署插件

## 配置_config.yml

---
## Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
type: git
repo: https://github.com/YourGithubName/YourGithubName.github.io.git
branch: master

-----
hexo d #部署到Github仓库里
https://YourGithubName.github.io/ #访问这个地址可以查看博客

git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia #下载yilia主题到本地

### 修改hexo根目录下的 _config.yml 文件 ： theme: yilia

hexo c #清理一下
hexo g #生成
hexo d #部署到远程Github仓库
https://YourGithubName.github.io/ #查看博客