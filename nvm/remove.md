# linux移除系统node

## 全局卸载npm

``` shell
npm uninstall npm -g
```

## 卸载node

``` shell
yum remove nodejs npm -y
```

## 移除残留

* 进入 `/usr/local/lib` 删除所有 node 和 node_modules文件夹
* 进入 `/usr/local/include` 删除所有 node 和 node_modules 文件夹
* 进入 `/usr/local/bin` 删除 node 的可执行文件
