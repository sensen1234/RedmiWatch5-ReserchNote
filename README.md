# RedmiWatch5-ReserchNote
RW5研究笔记  
本人设备为esim版，但此研究笔记大部分内容蓝牙版通用  
## 表盘（Vela小程序）安装提示无存储空间解决办法  
因为现在手表芯片被挖出来了为xring 所以米紧急更新了（大概率是）新的固件，限制了小程序安装  
目前网上最多的说法是最多可10小程序，但本人未成功复现  
如果系统软件版本为1.2.174(ESIM)  
请降级系统版本  
⚠️请使用Notify for Xiaomi降级系统，该应用可前往Google Play下载
*若无法访问GooglePlay 可前往"https://www.bandbbs.cn/threads/18497/"以及"https://www.bandbbs.cn/forums/notify/" 下载apks
1. download 1.1.157(https://www.bandbbs.cn/resources/2312/history#resflag)
      *固件在下载后为.zip格式，请勿解压  
2. 使用Notify for Xiaomi软件连接手表，并且选择固件并推送（由于推送的为完整包，蓝牙传输和升级时间会非常长，请耐心等待）  
   *该软件的连接设备，绑定方法请仔细阅读这个软件的提示  
   *固件升级在：Notify for Xiaomi——设备——升级固件——固件 中  
3. 升级完成后，先随便安装一个vela小程序（第三方），如果在安装的时候还是提示无存储空间，请先删掉一些自带小程序，确保其数量在10个以下
4. 在安装完后，就可以放心的在官方软件中升级到最新版本固件了，升级后就可突破10小程序的限制。
*实测还是会有限制，可安装程序数量大概为15个，如果有条件，还是继续在老版本好，比如1.1.163的版本  

在我本人测试中，有一定概率无法直接从1.2.174降级为1.1.163，所以我的建议是：  
先降级为1.1.157，全部操作完毕后再手动升级为1.1.163并日常使用（如果你用1.1.163的话）  
如果有更好的方法，欢迎提交issues和Pull requests  
*目前找到一种新的方法，但是有点大力砖飞.... 那就是：把多个vela应用，集合到一个应用里(x
##  Lua表盘制作
🐶🐔🌿的🐒工程师，把Lua表盘砍了，无解了...  
除非ota回来  
## 关于Esim版的芯片  
该表里有3个Xring芯片，并且有一个芯片支持WIFI6  
也不知道米工程师怎么想的，不开放WIFI功能  
如果想启用Xring，需要前往设置——网络与连接——移动网络——通讯（启动手表通讯能力）中启用  
开启之后会有些许的功耗增加  
如果你有感觉手表卡顿，可以试试启用这个来解决  
## 关于小程序兼容问题&是否可安装其他设备的vela小程序
理论来说是可以的，但可能会有UI bug  
在米的https://iot.mi.com/vela/quickapp 中，虽然没写有自动多屏适配功能  
## 1.2.174系统内部信息
MIIDazCCAlOgAwIBAgIUYxxnfse6kbtN9NpLJNiVPNwUo2MwDQYJKoZIhvcNAQEL
BQAwRTELMAkGA1UEBhMCQVUxEzARBgNVBAgMClNvbWUtU3RhdGUxITAfBgNVBAoM
GEludGVybmV0IFdpZGdpdHMgUHR5IEx0ZDAeFw0yMzEyMTMwMjU3MDhaFw0yNDA2
MTAwMjU3MDhaMEUxCzAJBgNVBAYTAkFVMRMwEQYDVQQIDApTb21lLVN0YXRlMSEw
HwYDVQQKDBhJbnRlcm5ldCBXaWRnaXRzIFB0eSBMdGQwggEiMA0GCSqGSIb3DQEB
AQUAA4IBDwAwggEKAoIBAQDYELKomcUcXRBwx/EmGAvf/Kx5wEX/CYorKWeJawOV
hCtAaCxTOiT1ZRAEhvDrlqNivtJ6Gl1P99m3Mm0MoeNVSHzOlLdDA4cIoIKZ98BP
wG1zY7YNk3ebscvdm+mtSoSC1sDjSIM7m8hNdpUxVQOS1EXqS6aUEgI0rbdvv261
A0ASgWv24tEOpXRcT7JQ8ZGGjiSr33u10AMkEWRw79FKraGXP4N0R4Zc/+inppmd
MDKqBlUGO80kWBRoO97rxwHY8xgIoVQWV64/6AJW0QzhnKwM6hKn3VBcowj2iZ7N
JF7HpkF+RxB2WzVRoiKeRHu3Fc9H95NjQxeNlEaF+s+XAgMBAAGjUzBRMB0GA1Ud
DgQWBBQaufeaLVvlU5FGZKUuKpWVtJuCTjAfBgNVHSMEGDAWgBQaufeaLVvlU5FG
ZKUuKpWVtJuCTjAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3DQEBCwUAA4IBAQBe
6vXs3f09Al7l/51zuSbyJa6laoPQZfCofRriN8nOd89hasupBqNEx1Du/zIt+/CA
b7tClG+C844BEnHxzUS73dxjQODeAq/7mi0gH+6rOgcfG2oKO7F5aMUV+HWTvbir
KaBc5pOJ4MiG5pUU3nMuoJz1ygvAK9G4E1JIQTPY7p2zcfYeGji6i4CUbFQ+n+Kz
yY+EqxgXQ1ajDk9XvMlAdCAD9J1Aapus87kxrEQrEhm8si252fnAlrQ58BnzleXK
We6me40oH7beZgZlyOla46GFcyrq0SrDvicfnM8uvlIg+u4BIbDfEdu/BLXyC8g5
MV7lwzdVE2/B1pDZyz68
-----END CERTIFICATE-----
但我用Aiot IDE测试，大部分是可以用的  
所以，如果你觉得5的程序少，可以试着把4的装进去（但可能有bug，若出问题本人不负任何责任）  
比如我就把4的五子棋（BYGiveMeFive）装到了5上，但是无BUG，完美运行  
