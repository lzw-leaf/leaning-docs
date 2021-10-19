# nrm

依赖于npm的一个npm依赖源替换包，可以快捷的更换npm的依赖源来方便开发。

> 当使用nvm安装多个node版本时，要想在所有的node版本生效，需要每个版本都安装。公用一个全局文件包，可能会造成依赖崩塌。

## install

npm全局安装

    npm i -g nrm

## 常用命令

描述 | 命令  
---|---
列出所有可更换依赖源 |  nrm ls
切换依赖源 | nrm use
测试指定源的响应时间 | nrm test
添加指定源 | nrm add [alias] [url]
删除指定源 | nrm del [alias] [url]
