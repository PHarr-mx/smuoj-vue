# smuoj-vue
西南民族大学oj 前端

## 日志

2024.09.1 

- 修复了修改密码页面的滑块验证码，将图片修改为本地图片
- 完成对logo的修改
- 去掉了自测功能以提高性能

2024.08.31 完成本地部署，对开发者界面做出一点修改

## 教程

首先要安装`nodejs`版本是`v14.21.3`，其次要安装`npm`版本是`6.14.18`

然后给`npm`换源

```sh
npm config set registry https://registry.npmmirror.com/
```

验证命令

```shell
npm config get registry
```

找到`vue.config.js`，根据72、73行的注释进行调整

然后在`/hoj-vue`目录下执行

```sh
npm install 
npm run serve
```

就可以在浏览器`http://localhost:6688`看到本地部署的前端

修改完成后，运行`npm run build`进行打包

```sh
 DONE  Build complete. The dist directory is ready to be deployed.
 INFO  Check out deployment instructions at https://cli.vuejs.org/guide/deployment.html
```

看到以上提示说明打包成功，把`dist`直接上传到服务去的`~/sumoj/`目录下，并重新执行`doceker compse up -d` 即可
