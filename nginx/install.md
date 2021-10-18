# install

## CentOS 源码安装

1. 从官网下载最新的nginx源码包并解压

[官网下载入口](http://nginx.org/en/download.html)

2. yum安装编译模块依赖

``` shell
# 安装依赖前最好更新本机的依赖到最新
yum update
yum install gcc gcc-c++ pcre pcre-devel zlib zlib-devel openssl openssl-devel -y
```

3. 执行编译脚本

``` shell
sudo ./configure  --prefix=/usr/local/nginx --with-threads --with-http_realip_module --with-http_stub_status_module --with-http_gzip_static_module --with-http_ssl_module --with-http_v2_module 
```

* --with-threads 开启多线程
* --with-http_realip_module 允许修改ip
* --with-http_stub_status_module 协议状态监控
* --with-http_gzip_static_module 加载压缩传输模块
* --with-http_ssl_module 加载https模块
* --with-http_ssl_module 加载http2模块

4. 编译安装

``` shell
make && make install
```
