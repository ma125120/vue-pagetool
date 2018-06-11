# vue-pagetool
使用node脚本快速搭建vue项目的基本结构

##安装
``` bash
$ npm install vue-pagetool
```

##使用

新建一个page.js,内容为：
```javascript

var { createPages } = require("vue-pagetool");
var page_model = {
  root_dir: './src',//指定src的目录
  pages: [{
    name: 'home',
    pages:[{
      name: 'login',
      components: ['top','head'],
      pages: [{
        name: 'test'
      }]
    },{
      name: 'signin'
    },{
      name: 'signup'
    }]
  }]
}

createPages(page_model);
```

之后运行
``` bash
$ node index.js
```
即可生成vue的项目模板，具体的结构大家可以先自行测试，如果觉得有什么不妥之处，欢迎指正！
