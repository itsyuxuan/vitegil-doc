# 功能需求

## 前言

在传统模式中，前端项目发布到生产环境后就成了一个 “黑盒”——报错信息依赖于用户发送截图或者口头告知开发者，然后开发者根据用户的描述去重现错误，这导致前端项目 debug 的效率十分低下。

因此，我们决定自研一套能够用于前端埋点监控 Web 页面关键运行数据并上报的 SDK 探针。

## 确定需求

1. 业务层
   1. UV/PV：页面访问量和访问人数
   2. 访问者信息：访问者的 IP、访问者的 UA、访问者的操作系统、访问者的浏览器、访问者的地区、访问者的语言、访问者地区、访问者的网络类型等
2. 网站性能
   1. 页面性能
   2. 页面响应时间
3. 错误监控
   1. JS 错误
   2. Promise 错误
   3. 资源加载错误
   4. 接口错误
   5. DOM 错误
4. 上报策略
   1. 定时上报
   2. 延迟上报
5. 使用策略：埋点无侵入式


