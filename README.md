# moon-tracker 月亮追踪器
这是一个上报uv，pv，监控异常的十分简洁易用的SDK插件，后续会添加更多用法😁
（目前moon-tracker还是基础版，如果想要使用更多用法，请使用更强大的tracker插件）

由于最近在看某些框架的官网，让我一个练习时长一坤年😬的人学习起来十分难受，很难理解
所以特地回来补充一下这个tracker用法，希望能够让人快速理解

通过npm install moon-tracker之后，你可以在你的main.js或者首页入口引入调用
```
import MoonTracker(名字随便取) from 'moon-tracker'

const tracker = new MoonTracker({
    uuid:'' // 后端返回的uuid身份标识
    requestUrl:'' // 填入你想上报的接口地址链接
    historyTracker: true // 开启history路由页面切换上报
    hashTracker: true // 开启hash路由变化上报
    domTracker: true // 想要使用dom点击或者移入移出等事件上报，需要为元素添加一个target-key的属性，属性值自己定义
    sdkVersion: // 这个版本无所谓，默认会传一个版本
    extra: // 想要传递的更多信息
    jsError: true // 开启js语法和promise错误，undefined之类，接口请求reject的promise异常
})

```
最后再介绍一下options
```
/**
 * @requestUrl 接口地址
 * @historyTracker history上报
 * @hashTracker hash上报
 * @domTracker 携带Tracker-key 点击事件上报
 * @sdkVersion sdk版本
 * @extra透传字段
 * @jsError js 和 promise 报错异常上报
 */
```