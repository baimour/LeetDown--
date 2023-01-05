# LeetDown
    
一个GUI MacOS应用程序，将兼容的A6和A7设备降级为OTA签名的固件
    
[![CI](https://img.shields.io/github/actions/workflow/status/rA9stuff/LeetDown/ci.yml?branch=master&style=for-the-badge)](https://github.com/rA9stuff/LeetDown/actions)
[![Stars](https://img.shields.io/github/stars/rA9stuff/leetdown?style=for-the-badge)](https://github.com/rA9stuff/LeetDown/stargazers)
[![Licence](https://img.shields.io/github/license/rA9stuff/leetdown?style=for-the-badge)](https://github.com/rA9stuff/LeetDown/blob/master/LICENSE.md)
<br/>
<img align="right" src="https://i.imgur.com/5lI2lIo.png" width="130px" height="130px">
### 下载
* [Latest notarized release (推荐)](https://github.com/rA9stuff/LeetDown/releases)
* [Nightly builds (实验)](https://nightly.link/rA9stuff/LeetDown/workflows/ci/master)


# 兼容   

### 兼容的iOS设备

| iOS 8.4.1 降级 | iOS 10.3.3 降级 |
| :---         | :---         |
| iPhone 5   | iPhone 5s   |
| iPad 4   | iPad Mini 2 (除了 J87AP)   |
| -   | iPad Air   |
   
   
### 兼容的MacOS

| Intel Macs    | ASi Macs (Rosetta 2) |
| --- | --- |
| MacOS 10.13 +   | MacOS 11.0 + |

### 虚拟机和黑苹果
LeetDown与虚拟机不兼容，一些黑苹果系统成功地运行了LeetDown，但是，利用您在真实Mac硬件以外的环境中遇到的问题取决于您的解决。请不要为此创建问题

# 安装

打开 `LeetDown_[VERSION].dmg` 并将 `LeetDown.app` 拖到 `/Applications` 文件夹

按照应用程序中显示的说明进行操作

# 疑难解答
### A7设备和Apple Silicon Mac

* 由于Asi Macs的USB堆栈，在LeetDown上传iBSS后，设备将消失。当您收到提示 `[+] 设备丢失，请将USB线重新连接到您的Mac以恢复上传过程`时，按照提示进行操作，降级将自动恢复
* 确保将数据线**重新连接到您的Mac**您无需将数据线重新插入iOS设备

### Stuck at exploiting or exploitation failure

* 确保您没有使用任何USB集线器或type-c到Lightning，如果您的Mac只有USB-C接口，请使用Lightning转type-a和type-c转type-a转换器
* 确保您没有在虚拟机下运行LeetDown，查看 [compatiblity](https://github.com/rA9stuff/LeetDown#compatibility)
* 重新进入DFU模式，并尝试使用LeetDown再次漏洞攻击
* 如果它仍然不起作用，[下载 iPwnder-lite](https://github.com/dora2-iOS/ipwnder_lite) 并手动利用漏洞攻击您的设备

### 无法降级设备

* 使用iTunes/Finder/idevicerestore更新至最新iOS版本，然后重试
* 检查USB线是否正常工作
* 尝试使用不同的USB接口 (或适配器，如果在Apple Silicon上运行)


# Build Instructions  
### With Xcode
`cd` to project directory   
run `pod install`   
open `.xcworkspace` and run it    

### With CLI
`cd` to project directory   
run `pod install`   
run `xcodebuild -workspace LeetDown.xcworkspace -scheme LeetDown_M` 

# 有问题？

* 通过点击LeetDown设置中的框启用调试模式
* 打开一个问题，填写模板并从 `~/Documents` 文件夹将 `LDLog.txt` 添加到其中

# 支持者  
* Will Kellner
* qqjqqj

# 致谢：

* [@axi0mX](https://twitter.com/axi0mX) for checkm8 exploit
* [@tihmstar](https://twitter.com/tihmstar) for futurerestore
* [@Cryptiiiic](https://twitter.com/Cryptiiiic) for updated futurerestore
* [@\_m1sta](https://twitter.com/_m1sta) for updated futurerestore
* [@dora2ios](https://twitter.com/dora2ios) for iPwnder-lite
* [@mosk_i](https://twitter.com/mosk_i) for iBoot patches and internal testing
* [@libimobiledev](https://twitter.com/libimobiledev) for libirecovery
* [@ConsoleLogLuke](https://twitter.com/ConsoleLogLuke) for helping with the dependencies and scripts for versions < 2.0
* [ZipArchive](https://github.com/ZipArchive/ZipArchive) for SSZipArchive
* [AFNetworking](https://github.com/AFNetworking/AFNetworking) for AFNetworking
* [@alitek123](https://twitter.com/alitek123) for OTA BuildManifests
* [@exploit3dguy](https://twitter.com/exploit3dguy) for private testing
* [@m3t0ski](https://twitter.com/m3t0ski) for private testing
* [@AyyItzRob123](https://twitter.com/AyyItzRob123) for private testing
* [Mini-Exploit](https://github.com/Mini-Exploit) for private testing
