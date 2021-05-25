# nacos-forward-proxy（未完成）

为PHP/PYTHON提供HTTP正向代理服务，将在每个应用容器中运行。

为应用代理HTTP请求，基于NACOS服务发现IP:PORT，进行带重试和熔断的请求调用。

健康探测容器内的应用端口，为应用代理注册至NACOS。

开发状态：

* HTTP/HTTPS正向代理：完成
* NACOS服务发现：TODO
* 熔断器：TODO
* NACOS服务注册：TODO

## 体验

HTTP协议正向代理：

```
curl --proxy http://127.0.0.1:1080 'http://www.baidu.com'  -I
```

HTTPS协议正向代理：

```
curl --proxy http://127.0.0.1:1080 'https://www.baidu.com'  -I
```