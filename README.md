# ts-vue-demo

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

参考博客： https://juejin.im/post/5d0259f2518825405d15ae62#heading-37

构建项目遇到的问题：

1. ERROR  command failed: npm install --loglevel error --registry=https://registry.npm.taobao.org --disturl=https://npm.taobao.org/dist

修改.vuerc 中 "useTaobaoRegistry": true, 改为false  （for mac: 找不到.vuerc的童鞋直接用命令打开：open .vuerc）

2. Experimental support for decorators is a feature that is subject to change in a future release. Set the 'experimentalDecorators' option to remove this warning.  (vscode语法错误）
 
 解决： https://www.jianshu.com/p/fd2f9caa64dd

