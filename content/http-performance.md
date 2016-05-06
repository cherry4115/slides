## HTTP 与 性能优化

<style>
.reveal .run-btn {display:none}
.box-model {width: 10em;height: 6em;background:#09c;box-shadow:#f80 0 0 0px 2em, #690 0 0 0 4em, #999 0 0 0 6em; margin: 6em auto 7.5em auto!important}
.box-model p {line-height: 2em; position: relative; top: -6em}
</style>

### 闻双云

---

### HTTP 位于 OSI 七层模型中的最上层 - 应用层
### 基于TCP

---

<div><img src="img/http-performance/tcp.jpg"></div>

---

### HTTP 状态码

* 200 OK *
* 301 Moved Permanently
* 302 Moved Temporarily
* 304 Not Modified *
* 401 Unauthorized
* 403 Forbidden
* 404 Not Found *
* 500 Internal Server Error
* 501 Not Implemented
* 502 Bad Gateway *

---

## HTTP 请求-响应过程

* 解析url，得到服务器的ip和端口号
* 建立与服务器的tcp连接
* 向服务器发送http请求报文
* 服务器返回http响应报文
* 关闭连接，显示文档

---

## 历史回顾

* HTTP 0.9 （1991） 响应超文本
* HTTP 1.0 （1996） 响应不限于超文本
* HTTP 1.1 （1999） 持久连接，缓存机制
* HTTP 2.0 （2015） 二进制请求头，多路复用

---

## 性能优化

* 减少HTTP请求数目 合并资源
* 多开几个TCP 并发请求
* 缓存 Last-Modified，Etag，Expires

---

<div><img src="img/http-performance/lastModified.jpg"></div>

---

<div><img src="img/http-performance/expires.jpg"></div>

---

<img src="img/http-performance/cache-control.jpg">

---

## Thanks
