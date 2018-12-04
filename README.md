

# vuejs-admin（设备管理系统）


> * 用户模块（用户管理）
> * 设备模块（设备管理、设备实时监控、设备参数记录、设备类别管理、参数管理等）
> * 授权模块（引入OAuth2.0授权服务，方便将接口以OAuth提供第三方）
> * 消息模块（用户申请帮助消息、设备参数告警消息）

## 技术栈

关键字

> * 前端：vuejs、vue-router、vuex、axios、element-ui、iconfont、mqttjs
> * 后端：eggjs、mysql、OAuth2.0、restful、nginx、mqtt、jwt（负责前端所有消息推送&设备实时参数接收）


## 源码说明
### 项目目录说明
```
.
|-- config                           // 项目开发环境配置
|   |-- index.js                     // 项目打包部署配置
|-- src                              // 源码目录
|   |-- components                   // 公共组件
|       |-- header.vue               // 页面头部公共组件
|       |-- index.js                 // 加载各种公共组件
|   |-- config                       // 路由配置和程序的基本信息配置
|       |-- routes.js                // 配置页面路由
|   |-- css                          // 各种css文件
|       |-- common.css               // 全局通用css文件
|   |-- iconfont                     // 各种字体图标
|   |-- images                       // 公共图片
|   |-- less                         // 各种less文件
|       |-- common.less              // 全局通用less文件
|   |-- pages                        // 页面组件
|       |-- home                     // 个人中心
|       |-- index                    // 网站首页
|       |-- login                    // 登录
|       |-- signout                  // 退出
|   |-- store                        // vuex的状态管理
|       |-- index.js                 // 加载各种store模块
|       |-- user.js                  // 用户store
|   |-- template                     // 各种html文件
|       |-- index.html               // 程序入口html文件
|   |-- util                         // 公共的js方法，vue的mixin混合
|   |-- app.vue                      // 页面入口文件
|   |-- main.js                      // 程序入口文件，加载各种公共组件
|-- .babelrc                         // ES6语法编译配置
|-- gulpfile.js                      // 启动，打包，部署，自动化构建
|-- webpack.config.js                // 程序打包配置
|-- server.js                        // 代理服务器配置
|-- README.md                        // 项目说明
|-- package.json                     // 配置项目相关信息，通过执行 npm init 命令创建
.
```

### 开发环境依赖模块说明
#### webpack相关模块
```
webpack                               // 用来构建打包程序
webpack-dev-server                    // 开发环境下，设置代理服务器
html-webpack-plugin                   // html 文件编译
url-loader                            // 图片  转化成base64格式
file-loader                           // 字体  将字体文件打包
css-loader                            // css  生成
less                                  // css  预处理器less
less-loader                           // css  预处理器less的webpack插件
style-loader                          // css  插入到style标签
autoprefixer-loader                   // css  浏览器兼容性问题处理
babel-core                            // ES6  代码转换器
babel-loader                          // ES6  代码转换器，webpack插件
babel-plugin-transform-object-assign  // ES6  Object.assign方法做兼容处理
babel-preset-es2015                   // ES6  代码编译成现在浏览器支持的ES5
babel-preset-stage-0                  // ES6  ES7要使用的语法阶段
vue-loader                            // vue  组件编译
babel-helper-vue-jsx-merge-props      // vue  jsx语法编译
babel-plugin-syntax-jsx               // vue  jsx语法编译
babel-plugin-transform-vue-jsx        // vue  jsx语法编译
```

## 目前进展

已完成

> * 用户登录、退出
> * 用户模块：用户列表（带分页）、新增、删除、编辑、头像上传等
> * 个人资料编辑设置
> * 设备模块：设备列表（带分页）、新增、删除、编辑等
> * 设备实时参数图表展现

TODO

> * 设备参数告警、参数管理等
> * OAuth2授权管理模块
> * 消息管理模块

## 构建

``` bash
# 安装依赖
npm install

# 测试运行
npm run dev

# 构建发布包
npm run build

# 构建并导出report
npm run build --report
```

## 测试账号

caiya928@aliyun.com/admin

ps: 大家别乱搞啊，要不服务就关停了

## 效果图

![登录](https://raw.githubusercontent.com/caiya/imgs/2a33e9a186536903ac75bcae5cffb9274876462f/dev-login.png)

![主页（登录后）](https://raw.githubusercontent.com/caiya/imgs/2a33e9a186536903ac75bcae5cffb9274876462f/dev-main.png)

![用户列表页](https://raw.githubusercontent.com/caiya/imgs/2a33e9a186536903ac75bcae5cffb9274876462f/dev-users.png)

![用户新增&编辑](https://raw.githubusercontent.com/caiya/imgs/2a33e9a186536903ac75bcae5cffb9274876462f/dev-user-add.png)

![设备列表](https://raw.githubusercontent.com/caiya/imgs/2a33e9a186536903ac75bcae5cffb9274876462f/dev-devices.png)

![设备新增&编辑](https://raw.githubusercontent.com/caiya/imgs/2a33e9a186536903ac75bcae5cffb9274876462f/dev-device-edit.png)

![设备类型](https://raw.githubusercontent.com/caiya/imgs/2a33e9a186536903ac75bcae5cffb9274876462f/dev-devtypes.png)

![设备监控](https://raw.githubusercontent.com/caiya/imgs/41f4765c49f7f1f93fed35b3a2099c8e16f1ba93/s-11.png)

![实时展现](https://raw.githubusercontent.com/caiya/imgs/41f4765c49f7f1f93fed35b3a2099c8e16f1ba93/s-22.png)

