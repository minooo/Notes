## node是什么
    node旨在提供一种简单的构建可伸缩网络程序的方法。
    node是一个服务器端的JavaScript的解释器。
    
## npm是什么
    npm是包管理器，包括安装，卸载，更新，查看，搜索，发布等。
    npm的背后，是基于couchdb的数据库，详细记录了每一个包的相关信息，包括作者，版本，依赖，授权。
    它的作用就是将开发者从繁琐的包管理工作（版本，依赖等）中解放出来，更加专注于功能开发。
    
- npm help 呼出所有npm相关命令
- npm 包括本地安装和全局安装（-g),每个包安装后，控制台输出信息包括这个包的版本，安装位置，如果有依赖，还会有依赖的版本号
- 安装 npm install
- 卸载 npm uninstall XXX, 卸载指定版本号 npm uninstall XXX "15.1" 
- 查看 npm ls；查看全局安装信息 npm -g ls；查看特定包 npm ls react；查看详细信息 npm info react；
- 更新 npm update react
- 搜索 npm search react