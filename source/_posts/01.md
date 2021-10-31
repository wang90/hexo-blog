---
title: 构建自己的 hexo 博客
date: 2021-10-23 16:32:29
tags: hexo
---

## 记录我升级成 hexo 博客的第一天
因为服务器到期了，再加上最近想搞一些自己的东西，所以重新弄下博客，为了快捷方便，我选择的解决方案是 hexo + github

### 构建 hexo 博客

1. 下载 hexo-cli
``````
npm install hexo-cli -g
``````
因为国内比较慢我用的是
``````
cnpm install hexo-cli -g
``````
2. 下载完成后创建
``````
hexo init blog
cd blog
npm install
``````
3. 启动
``````
hexo serve
// or
npm run start 
// open 
// http://localhost:4000/
``````


### 编辑
1. 创建新文章
`````
hexo new 'first blog'
`````
2. 编辑
`````
/*  
* 编辑在 source/_posts文件夹下面的 md
***/
`````

### 发布
1. 配置 github
`````
vi _config.yml
`````
2. github 相关点
``````
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: git
  repo: git@github.com:wang90/wang90.github.io.git
  branch: master
``````
3. 推送
``````
hexo deploy
``````

### 更换主题
1. 打开 [https://hexo.io/themes/](https://hexo.io/themes/) 
2. 选择自己喜欢的主题文件下载保存至 themes 中
3. 修改 _config.yml 文件 theme: xxx
* 需要因为我是保存至 github actions 进行部署，所以thems中有个 .gitweek 使得文件无法全部提交
