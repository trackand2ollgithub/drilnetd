## BND1

[又一个百度网盘不限速下载器 BND](https://hacpai.com/article/1524460877352)

![bnd1](https://user-images.githubusercontent.com/873584/52854939-0825f100-315b-11e9-9aca-d03841b6c44e.png)

* 小巧省资源
* 支持 Linux、支持 32 位的 Windows

### 代码

本项目是基于 [BaiduPCS-Go](https://github.com/iikira/BaiduPCS-Go) 开发：

* 在其基础上增加了 UI 界面，主要修改点是 pcscommand 包
* Windows 版引入了 Aria2，下载超过 512M 文件时会切换到 Aria2

### 编译

1. 安装 golang 环境
2. 项目目录 $GOPATH/src/github.com/b3log/bnd
3. 参考 https://github.com/andlabs/libui 编译 UI 库
4. 不支持交叉编译，只能在目标平台上编译
5. Windows 执行 build.bat，Linux/Mac 执行 build.sh

### 其他

* aria2 原有设计是在启动后检查版本并远程拉取的，现已改为本地打包
* 保留了版本检查机制，可搜索 rhythm.b3log.org 进行相关修改
* 和服务端交互时用于加密请求响应数据的密钥已在源码中公开

### 鸣谢

* [aria2](https://github.com/aria2/aria2)：超高速的下载引擎
* [BaiduPCS-Go](https://github.com/iikira/BaiduPCS-Go)：百度网盘客户端 - Go 语言编写
* [andlabs/ui](https://github.com/andlabs/ui)：跨平台的 Go GUI 库
