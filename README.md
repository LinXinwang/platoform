# studybyzero   2020/11/25

  + learn how to create a vue.js project
  + In depth interpretation of the project structure
  + master the write rule of .md file

## Build Setup

``` creat a vue project
step one: npm install -g vue-cli   （if you have installed the vue-cli, ignore this step）
step two: vue init webpack studybyzero
step three: cd studybyzero
step four: npm run dev
```


``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

``` structure
1、build：构建脚本目录
　　1）build.js   ==>  生产环境构建脚本；
　　2）check-versions.js   ==>  检查npm，node.js版本；
　　3）utils.js   ==>  构建相关工具方法；
　　4）vue-loader.conf.js   ==>  配置了css加载器以及编译css之后自动添加前缀；
　　5）webpack.base.conf.js   ==>  webpack基本配置；
　　6）webpack.dev.conf.js   ==>  webpack开发环境配置；
　　7）webpack.prod.conf.js   ==>  webpack生产环境配置；
2、config：项目配置
　　1）dev.env.js   ==>  开发环境变量；
　　2）index.js   ==>  项目配置文件；
      （1）module.exports配置中找到autoOpenBrowser，改为true，执行 npm run dev 就会自动打开浏览器。
      （2）module.exports 配置中找到 port: 8080，可修改端口。
　　3）prod.env.js   ==>  生产环境变量；
3、node_modules：npm 加载的项目依赖模块（依赖包都在这里）
4、src：这里是我们要开发的目录，基本上要做的事情都在这个目录里。里面包含了几个目录及文件：
　　1）assets：资源目录，放置一些图片或者公共js、公共css。这里的资源会被webpack构建；
　　2）components：组件目录，我们写的组件就放在这个目录里面；
　　3）router：前端路由，我们需要配置的路由路径写在index.js里面；
　　4）App.vue：根组件；
　　5）main.js：入口js文件；
5、static：静态资源目录，如图片、字体等。不会被webpack构建
6、index.html：首页入口文件，可以添加一些 meta 信息等
7、package.json：npm包配置文件，定义了项目的npm脚本，依赖包等信息
8、README.md：项目的说明文档，markdown 格式
9、.xxxx文件：这些是一些配置文件，包括语法配置，git配置等

```
``` markdown grammar
    #一级标题，##是二级标题，以此类推。支持六级标题
    **这是加粗的文字**
    *这是倾斜的文字*`
    ***这是斜体加粗的文字***
    ~~这是加删除线的文字~~
    引用的文字前加>即可
    ---
    分割线1
    ----
    ***
    分割线2
    *****
    图片 ![blockchain](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=702257389,1274025419&fm=27&gp=0.jpg "区块链")

    [超链接名](超链接地址 "超链接title") title可加可不加
    [简书](http://jianshu.com)

    无序列表
    - 列表内容
    + 列表内容
    * 列表内容

    表格（左对齐--- 居中对齐:--:  右对齐---:）
    表头|表头|表头
    ---|:--:|---:
    内容|内容|内容
    内容|内容|内容

    代码
    单行代码
    `create database hero;`
    多行代码
    (```)
        function fun(){
             echo "这是一句非常牛逼的代码";
        }
        fun();
    (```)

    流程图
    ```flow
    st=>start: 开始
    op=>operation: My Operation
    cond=>condition: Yes or No?
    e=>end
    st->op->cond
    cond(yes)->e
    cond(no)->op
    ```
```
