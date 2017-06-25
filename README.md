# Vue2.0全家桶仿腾讯新闻
刚接触Vue，就自己动手撸了一个项目，项目可能不成熟，请大家多提意见

## 效果预览：
## 在线预览  [Vue之仿腾讯新闻](https://designdacity.github.io/news-preview/)
## 源码地址 [Github](https://github.com/designdacity/vue-news) 求您的star~
# 描述

## 技术栈
**Vue2**：采用最新Vue2的语法

**Vuex**：状态管理，实现不同组件之间的状态共享

**vue-router**：路由管理，实现路由的跳转

**axios**：发起http请求

**Express**：处理跨域请求问题

**Webpack**：自动化构建工具，大部分配置vue-cli脚手架已经弄好了，很方便

**淘宝flexible**：通过改变font-size,利用rem解决移动端适配问题

# 路由结构
```
routes: [
    {
      path: '/',
      component: index
    },
    {
      path: '/detail',
      name: 'detail',
      component: detail
    },
    {
      path: '/collectDetail',
      name: 'collectDetail',
      component: collectDetail
    },
    {
      path: '/channelManage',
      component: channelManage
    },
    {
      path: '/search',
      component: search
    },
    {
      path: '/searchDetail',
      name: 'searchDetail',
      component: searchDetail
    },
    {
      path: '/collection',
      component: collection
    },
    {
      path: '/msg',
      name: 'Msg',
      component: Msg
    }
  ]
```

## 使用 Build Setup

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
## 遇到的问题
* 异步编程问题：本项目使用了极速数据的API，后端的API编写也要解决请求数据的异步问题，JS实现异步的方法有`回调`、`Generator`、`Promise`、`Async`。
  回调层次多了，有回调地狱问题，代码的重用性、可观性不好；Generator需要手动执行（`co`模块可解决），相比之下，`Promise`和`Async`是比                 较理想的。
* 组件之间通信问题: 父组件可以通过props属性给子组件通信，子组件通过监听、触发事件向父组件通信，那兄弟组件呢？Vue2.0有eventBus解决这个问题，但是本人   还是特别喜欢用vuex，vuex将状态集中管理。
## 最后
[感兴趣请点我](os35cjzya.bkt.clouddn.com)



