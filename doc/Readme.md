# WebRTC基础

## 参考资料

WDN Web Docs 
https://developer.mozilla.org/zh-CN/docs/Web/API/WebRTC_API

Google WebRTC 
https://webrtc.org

## WebRTC的基本概念

WebRTC (Web Real-Time Communications) 是一项实时通讯技术，它允许网络应用或者站点，在不借助中间媒介的情况下，建立浏览器之间点对点（Peer-to-Peer）的连接，实现视频流和（或）音频流或者其他任意数据的传输。WebRTC包含的这些标准使用户在无需安装任何插件或者第三方的软件的情况下，创建点对点（Peer-to-Peer）的数据分享和电话会议成为可能。

### WebRTC中使用的协议介绍

#### ICE

交互式连接设施Interactive Connectivity Establishment (ICE) 是一个允许你的浏览器和对端浏览器建立连接的协议框架。在实际的网络当中，有很多原因能导致简单的从A端到B端直连不能如愿完成。这需要绕过阻止建立连接的防火墙，给你的设备分配一个唯一可见的地址（通常情况下我们的大部分设备没有一个固定的公网地址），如果路由器不允许主机直连，还得通过一台服务器转发数据。ICE通过使用以下几种技术完成上述工作。

##### STUN

NAT的会话穿越功能Session Traversal Utilities for NAT (STUN) (缩略语的最后一个字母是NAT的首字母)是一个允许位于NAT后的客户端找出自己的公网地址，判断出路由器阻止直连的限制方法的协议。

客户端通过给公网的STUN服务器发送请求获得自己的公网地址信息，以及是否能够被（穿过路由器）访问。

![avatar](https://github.com/baggiowangyu/BgRTC/blob/main/doc/img/webrtc-stun.png)

##### NAT

##### TURN

##### SDP