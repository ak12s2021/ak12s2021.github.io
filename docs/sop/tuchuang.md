---
description: 博客相关
title: 🔧 图床
readingTime: false
tag:
 - 博客
recommend: 3
---

# 图床加速图片加载的原理揭秘

在当今互联网时代，网站的加载速度至关重要，尤其是包含大量图片的页面。为了提升用户体验，很多网站选择使用图床来存储和加载图片。本文将深入探讨图床对图片加载速度的加速原理。

## 什么是图床？

图床是专门用于存储和分享图片的服务。与传统的服务器相比，图床通常具备更高的带宽和更优的性能，能够更快速地处理大量的图片请求。

## 加速原理

1. **内容分发网络（CDN）** 
    图床通常会结合CDN技术，将图片存储在全球各地的服务器上。当用户请求图片时，CDN会自动选择离用户最近的服务器进行响应，从而减少延迟并加快加载速度。
2. **优化图片格式**
    图床会对上传的图片进行格式优化，比如使用WebP等高效格式，降低文件大小，同时保持良好的视觉质量。这种优化不仅减少了数据传输量，也加速了加载过程。
3. **懒加载技术**
    很多图床支持懒加载功能，只有当用户滚动到页面中的图片时，才会开始加载。这意味着在初始加载时，浏览器只需处理可见区域的内容，从而进一步提高页面加载速度。
4. **并发处理**
    图床通常能够同时处理多个图片请求，提升了并发加载的能力。这对于有大量图片的页面尤其重要，可以显著减少整体加载时间。
5. **缓存机制**
    图床利用缓存机制，将常用的图片存储在用户的浏览器中或CDN的边缘节点上。这样，用户访问相同图片时，可以直接从缓存中获取，避免重复加载。

![](https://cbt567.top/wp-content/uploads/2024/09/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE-2024-09-18-100755.jpg)
#### 具体步骤

1. [阿里云oss](https://oss.console.aliyun.com/overview)

    1. 建立Bucket（文件夹类似）

1. ![](https://cbt567.oss-rg-china-mainland.aliyuncs.com/img/202507111746143.png)
2. [申请RAM](https://ram.console.aliyun.com/users)用户

    1. ![](https://cbt567.oss-rg-china-mainland.aliyuncs.com/img/202507111749803.png)
3. [下载picgo](https://picgo.github.io/PicGo-Doc/zh/guide/)
4. 输入上面生成的密钥和bucket

    ![](https://cbt567.oss-rg-china-mainland.aliyuncs.com/img/202507111803837.png)
5. 应用

    ![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/picgo-2.0.gif)