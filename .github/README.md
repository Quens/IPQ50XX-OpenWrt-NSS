本仓库基于 kuncy7/openwrt-nss-edma：OpenWrt 主线、内核 6.18

加上高通 NSS 硬件加速（有线 NAT、Wi-Fi offload、PPPoE、VLAN、SQM 队列），以太网走上游的 stmmac 驱动。

镜像只带日常必需的部分：中文 LuCI（Aurora 主题）及内存压缩交换（zram）；

如需其他插件（UPnP、DDNS、WireGuard、SQM 页面、网页终端等）请自己安装。

默认设置：

路由器地址192.168.10.1

wifi默认开启

名称：OpenWrt&OpenWrt-5G

密码：12345678。 


特别鸣谢：

1、Kuncy7 对IPQ50XX系列的NSS适配

https://github.com/kuncy7/openwrt-nss-edma

2、FlyFish-go对H3C-Magic RC3000系列机型OpenWrt的适配

https://github.com/FlyFish-go/H3C-Magic-NSS
