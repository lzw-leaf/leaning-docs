# install

## CentOS 源码安装

1. 从官网下载最新的nginx源码包并解压

[官网下载入口](http://nginx.org/en/download.html)

``` shell
wget  http://nginx.org/download/nginx-1.21.3.tar.gz ## 可以从上面官网找最新版本下载
tar zxvf nginx-1.21.3.tar.gz  ## 解压
cd nginx-1.21.3
```

2. yum安装编译模块依赖

``` shell
# 安装依赖前最好更新本机的依赖到最新
yum update
yum install gcc gcc-c++ pcre pcre-devel zlib zlib-devel openssl openssl-devel -y
```

2.1 GeoIP2数据库安装

### 依赖安装

``` shell
yum install libmaxminddb libmaxminddb-devel -y
```

### 编译安装

``` shell
wget https://github.com/maxmind/libmaxminddb/releases/download/1.6.0/libmaxminddb-1.6.0.tar.gz
tar zxvf libmaxminddb-1.6.0.tar.gz
cd libmaxminddb-1.6.0/
./configure
make
make check
make install
ldconfig
```

3. 执行编译脚本

``` shell
sudo ./configure  --prefix=/usr/local/nginx --with-stream --with-threads --with-http_realip_module --with-http_stub_status_module --with-http_gzip_static_module --with-http_ssl_module --with-http_v2_module  --add-module=/usr/local/ngx_http_geoip2_module 
```

* --with-stream 启动传输流
* --with-threads 开启多线程
* --with-http_realip_module 允许修改ip
* --with-http_stub_status_module 协议状态监控
* --with-http_gzip_static_module 加载压缩传输模块
* --with-http_ssl_module 加载https模块
* --with-http_v2_module 加载http2模块
* --add-module=/usr/local/ngx_http_geoip2_module  加载geoip2模块 (可选可去掉)

4. 编译安装

``` shell
sudo make && sudo make install
```
