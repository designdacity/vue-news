# Vue2.0全家桶仿腾讯新闻
刚接触Vue，就自己动手撸了一个项目，项目可能不成熟，请大家多提意见

## 在线预览  [Vue之仿腾讯新闻](https://designdacity.github.io/news-preview/)
## 源码地址 [Github](https://github.com/designdacity/vue-news) 欢迎大家star和fork :blush:
# 描述

## 技术栈
**Vue2**：前端页面展示。

**Vuex**：Vuex，实现不同组件间的状态共享

**vue-router**：路由管理，实现路由的跳转

**axios**：一个基于 Promise 的 HTTP 库，向后端发起请求。

**ES6**:采用ES6语法，这是以后的趋势。箭头函数、Promise等等语法很好用。

**Express**：处理跨域请求问题

**CSS3**：CSS3过渡动画及样式。

**Webpack**：vue-cli自带Webpack，但是需要自己改造一下，比如要对需要安装sass相关loader，vue-cli已经配置好了webpack，你只需要安装依赖就可以，使用的时候只需要<style lang="scss"></style>。

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
# 总结

1.组件状态多了用Vuex管理很方便，引用 Redux 的作者 Dan Abramov 的话说就是：
>Flux 架构就像眼镜：您自会知道什么时候需要它。

2.事先一定要先想好整个页面组成，怎样去分组件开发，这样在开发阶段会事半功倍。
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
[感兴趣请点我](http://os35cjzya.bkt.clouddn.com/%E9%9B%B7%E6%AF%85%E7%9A%84%E7%AE%80%E5%8E%86%20%281%29.pdf)



