# pwa-prelude

### 项目介绍
此项目为渐进式网页应用程序（PWA）的一个基础知识的介绍，其中包括主要分为两个部分

* PWA的基本概念，产生的背景，当前活跃度，应用场景及发展趋势。
* 简易PWA的搭建

#### PWA介绍
##### 概念及背景
PWA全称为Progressive Web App，即渐进式网页应用程序，它是Google在2015年提出的，直到2016年6月才推广的项目。为什么说是渐进式呢，因为新技术的标准支持度还不完全，可以逐步地支持新技术来改善用户体验。

PWA结合了一系列的新的web技术，实现了和原生应用相近的用户体验。
它具有以下特点：

	1.可靠
		当用户从手机主屏幕启动时，在网络环境差甚至无网络环境下也能瞬间加载并展现；(依赖Service Worker 技术)
	2.快速
		快速响应，并且有平滑的动画响应用户的操作（依赖App Shell）
	3.粘性
		像设备的原声应用，具有沉浸式的用户体验，可以添加到桌面(依赖Web App Manifest和Push Notification)

##### 关键技术
PWA不是一种新技术，而是一系列新的技术集合，其中关键的技术包括以下三个：

	1. Service Worker
	2. Manifest
	3. Push Notification

简要介绍下这三种技术。

* Service Worker

W3C 组织早在 2014 年 5 月就提出过 Service Worker 这样的一个 HTML5 API ，主要用来做持久的离线缓存。它的特性有以下几点：

1. 独立于主线程的worker线程，因此不会阻塞主线程的运行；
2. 不同于Web Worker,Service Worker 是持久化的，一旦被install，就会一直存在，除非手动注销；
3. 可以用来代理请求，可缓存文件，并且可供网页进程取用（离线状态也可以）；
4. 灵活触发，需要时候调起，不需要时睡眠
5. 必须在HTTPS环境工作；
6. 能向客户端推送消息。

详细的基本运行机制请看：


* Manifest(应用清单)

Web App Manifest 是一个 W3C 规范，它定义了一个基于 JSON 的 List。通过配置manifest,可以实现以下功能：

1. ​ 能够将你浏览的网页添加到你的手机屏幕上

2.  在 Android 上能够全屏启动，不显示地址栏 （ 由于 Iphone 手机的浏览器是 Safari ，所以不支持哦）
3. 控制屏幕 横屏 / 竖屏 展示
4. 定义启动画面
5. 可以设置你的应用启动是从主屏幕启动还是从 URL 启动
6. 可以设置你的应用启动是从主屏幕启动还是从 URL 启动

详细的基本运行机制请看：

* Push Notification

使用推送消息通知，能够让我们的应用像 Native App 一样，提升用户体验。

​ Push 和 Notification 是两个不同的功能，涉及到两个 API 。

​ Notification 是浏览器发出的通知消息。

​ Push 和 Notification 的关系，Push：服务器端将更新的信息传递给 SW ，Notification： SW 将更新的信息推送给用户。

​ 

​ 












