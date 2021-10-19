# 安装

## 配合nvm的话可以通过yum安装

> 默认情况下centOS中的yum包库内是没有yarn的需要如下命令添加

``` shell
curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
```

## 安装

``` shell
yum install yarn
source /etc/profile
```
