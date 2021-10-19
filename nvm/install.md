# nvm

## 安装

> 前置条件：需要按照 git

从github的镜像库上克隆源码到 ~/.nvm

    git clone git://github.com/nvm-sh/nvm.git  ~/.nvm

检测分支和最新版本

    cd ~/.nvm && git checkout `git describe --abbrev=0 --tags`

将环境变量写入~/bashrc文件

    
    # nvm
    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

## 相关命令 

描述 | 命令
---|---
检测版本 | nvm --version
检测远端node版本列表| nvm ls-remote
安装node版本 |  nvm install 12.16.3
切换node版本| nvm use 10.8.3
设置默认node版本|nvm alias default 12.16.3

## 配置

nvm更改node安装镜像源

    
    export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node
