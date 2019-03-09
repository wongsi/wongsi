使用Gitee+Hexo搭建blog

1. 安装Hexo

`sudo npm install -g hexo`

2. hexo初始化

```
hexo init blog
cd blog
```

3. 本地预览博客

编译项目，输入命令：`hexo g`

运行项目，输入命令：`hexo s`

在浏览器中输入`http://localhost:4000/``就可以看到效果啦

4. 部署博客到Gitee上

gitee.com上创建一个仓库, 修改配置文件`_config.yml`

```
deploy:
  type: git
  repo: https://gitee.com/wongsi/blog.git
  branch: master
```

输入命令`npm install hexo-deployer-git --save` 安装自动部署发布工具
输入命令`hexo clean && hexo g && hexo d` 发布博客，首次发布需要在shell中输入账号和密码。


## 扩展

1. [主题](https://hexo.io/themes/)

`git clone https://github.com/Mitscherlich/hexo-theme-amber.git themes/amber`

Then modify you _config.yml:

```
## Theme
theme: amber  # this enable your theme config
```

Enjoy your writing!

`hexo clean && hexo serve`