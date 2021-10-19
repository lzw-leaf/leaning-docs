# python3安装

## 前置依赖

``` shell
yum install gcc gcc-c++ pcre pcre-devel zlib zlib-devel openssl openssl-devel -y

```

[官网下载地址](https://www.python.org/downloads/)

``` shell
# 下载源码包以上面链接官网最新为准
wget https://www.python.org/ftp/python/3.10.0/Python-3.10.0.tgz 
# 解压
tar zxvf Python-3.10.0.tgz
# 进入目录并进行配置
cd Python-3.10.0 && ./configure --with-ssl --prefix=/usr/local/python3
# 编译并安装
make && make install

#建议软连接
ln -s /usr/local/python3/bin/python3 /usr/bin/python3
ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3
```
