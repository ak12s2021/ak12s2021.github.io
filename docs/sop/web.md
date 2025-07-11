---
description:  如何搭建网站
title: 🔧基于个人经验的Blog/网站搭建
readingTime: Ture
tag:
 - 网站搭建
 - blog
recommend: 3
sticky: 3
---

# 基于个人经验的Blog/网站搭建

## **结论**

|             | 阿里云+WordPress                             | Github page                                                |
| ------------- | ---------------------------------------------- | ------------------------------------------------------------ |
| 难度        | 🌟🌟开箱即用                                 | 🌟🌟🌟🌟🌟掉头发                                           |
| 使用难度    | 🌟简单，有仪表盘可视化，点点点就行           | 🌟🌟🌟难，需要会markdown知识和git知识                      |
| 价格/元     | 100左右                                      | 0-20之内                                                   |
| 实现难度    | 开箱形式复杂，不需要太多计算机相关知识       | 技术相对复杂，需要掌握Git与一点前端知识                    |
| 施工时间    | 2d                                           | 1h                                                         |
| 安全性(SSL) | 自己去阿里云平台申请CA，每三个月申请一次     | GitHub Pages 通过 Let's Encrypt 自动为自定义域名提供 HTTPS |
| 可扩展性    | 非常强，且简单（网上有大量的轮子可以直接用） | 很强，但是需要有前端知识2333，而且很难                     |
| 便捷性      | 由于使用了WordPress，在手机上都可以更新博客  | 只有配置好环境的电脑才可以编写博客                         |
| 主题        | 有丰富多彩的主题选择，开箱即用               | 主题同样丰富，但是需要配置                                 |


## 流程

1. 搭建/复制服务器，网站层
2. 进行部署
3. 购买域名
4. DNS解析


### 1+2部署层面

#### 阿里云+WordPress

1. 购买服务器 [阿里云官网](https://ecs.console.aliyun.com/home#/) 2核2G 3M带宽云服务器ECS
2. 用宝塔linux部署进服务器
3. 登陆宝塔平台，并构建wordpress环境
4. 完成

[参考](https://crowya.com/125)

#### Github page

[主题配置](https://theme.sugarat.top/config/frontmatter.html)

[使用 GitHub/Gitee Pages 部署博客](https://theme.sugarat.top/sop/gh-pages.html)


### 域名

[阿里云购买](https://wanwang.aliyun.com/domain)

### DNS解析


用阿里云控制台进行


## 科普/知识

##### DNS (Domain Name System)

进行主机名到IP地址的转换。简单来说就是让其他人也知道你网站在哪里。

主机名就是比如baidu.com

ip地址就是 122.122.122.1

**显而易见，主机名更方便人类记忆和体现网站的个性**


✓ 一个由分层的DNS服务器实现的分布式数据库。

✓ 允许主机查询分布式数据库的应用层协议。


域名分为不用等级，我们购买的时候先看顶级域。比如`.net .cn . com .top `等等，然后前面的前缀是我们可以自定义的

比如我现在的域名`ak12s.icu` 以及`cbt567.top`


![](http://127.0.0.1:6806/assets/image-20241204182418-5tvo78k.png)


![](http://127.0.0.1:6806/assets/image-20241204183938-hdr7bmq.png)

##### 网站的底层逻辑

一个服务器存放着你的网页文件与数据库（静态资源），然后DNS服务器来解析你的主机名。

* 阿里云+WordPress等于这些都是你的，这些东西你了如指掌

* Github page 等于github帮你托管服务器，你只需要搞个域名就行


##### 服务器

这里指一个有公网ip，linux系统的计算机

公网ip=所有人都可能能访问

linux系统=类似window/mac OS的操作系统 ，常见的有CentOS和Ubuntu


为什么我们部署在阿里云上的是宝塔linux？

它图形化可交互，你点点点就完了，你也不想看一堆乱七八糟的代码吧。

