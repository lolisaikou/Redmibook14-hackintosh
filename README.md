# RedmiBook 14增强版 OC引导

## 硬件信息：
以下信息来自官网
|   硬件   |                      详细信息                      |
| :------: | :------------------------------------------------: |
|  处理器  |           intel Core i5-10210U @ 1.60GHz           |
|   显卡   |           Nvidia GeForce MX250 ( 2 GB )            |
|   内存   |             板载8GB 2666MHz（不可更换）            |
|   硬盘   |                   512GB SATA固态                   |
|   声卡   |                  Realtek ALC256M                   |
|   网卡   |               intel Wireless-AC 9462               |

## 驱动情况：
  
#### 无解的：  
  
- 显卡无解已屏蔽  
- 麦克风无解（内置和耳机都无法驱动）  
- 接力，隔空传送目前无解（蓝牙可以正常被驱动）  

  
#### 正常的：  
  
- 外放和耳机已使用自己仿冒的AppleALC驱动（偶现电流音，需要重启或重载驱动）
- 网卡已使用[itlwm](https://github.com/OpenIntelWireless/itlwm/)中的itlwmx驱动（使用[commit #9da56de](https://github.com/OpenIntelWireless/itlwm/tree/9da56de0c1101da4e8249c16a78ded71fa974127)编译）  
- 触摸板正常  
- 蓝牙正常  
  
#### 不正常的：  
  
- 内置键盘<kbd>Alt</kbd>（<kbd>Option</kbd>）和<kbd>Win</kbd>（<kbd>Command</kbd>）的位置被交换了（外接不会）  
- 无法使用快捷键调节亮度  
- 长时间睡眠可能会睡死  
  
## 一些小提示：  
  
- 使用黑果小兵10.15.6（19G73）安装  
- 无线网卡网速网速只有20Mbps左右（2.5Mb/s），此为itlwm驱动的问题，只能等待后续修复。
- 使用手机usb共享200Mbps网速可以拉满哦  
- 不会自动连接WiFi，你可以(建议在windows下使用notepad++)修改OC\Kexts\itlwmx.kext\Contents\Info.plist配置文件，搜索WiFiConfig修改默认的WiFi配置，password下面的是密码，ssid下面的是WiFi名称  
- 项目下的HeliPort.zip（8月13日代码构建）是itlwm配套的客户端（只能帮助你扫描连接Wifi，不能自动连接）  
- 如果你觉得我仿冒的声卡驱动不行，教程在[这里](https://blog.daliansky.net/Use-AppleALC-sound-card-to-drive-the-correct-posture-of-AppleHDA.html)，还有我整理好的文件也都一起放在项目下的tools.zip压缩包里了(包含codec，节点图，供你参考；还有一些小工具绝对很好用)(哪位大佬能把麦克风驱动了我感激不尽啊！！！)！  
