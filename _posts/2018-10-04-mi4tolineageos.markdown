---
layout:     post
title:      "Mi4的LineageOS新生"
subtitle:   "小米4 Lineage OS 新生"
date:       2018-10-04 00:01:00
author:     "antknox"
header-img: "img/post-bg-2018.jpg"
tags:
    - IT

---
## 前言
终于,2018年9月14日，官方公告停止维护米4系列MIUI体验版、开发版，虽可预约升级稳定版，但已无意义。于是,就有了的米4的Lineage OS的新生!

相关:

1. [[ROM] 小米手机4官方ROM下载地址汇总（官方停止维护，本帖终结）	](http://www.miui.com/thread-10813361-1-1.html)
2. [小米手机4 MIUI7、MIUI6、MIUI V5官方刷机包汇总](http://www.miui.com/thread-7981186-1-1.html)

## 正文

1. 生前
  
   miui遗照

![小米手机4](/img/in-post/post-mi4tolineageos/001-1-小米手机4.png)

   米4的遗物  

![小米手机4-卡刷包](/img/in-post/post-mi4tolineageos/001-2-小米手机4-卡刷包.png)

[小米手机4-卡刷包](http://www.miui.com/download-241.html)

![手机是否是BL锁](/img/in-post/post-mi4tolineageos/001-3-手机是否是BL锁.png)

![小米手机4-线刷包](/img/in-post/post-mi4tolineageos/001-4-小米手机4-线刷包.png)

[小米手机4-线刷包](http://www.miui.com/shuaji-393.html) & [线刷工具- 通用刷机工具点击下载](http://bigota.d.miui.com/tools/MiFlash2018-5-28-0.zip)

2. 准备  

	1.  解锁的手机&备份好手机数据
	2.  PC
	3.  ADB工具&Fastboot工具
	4.  第三方的Recovery TWRP
	5.  第三方ROM Lineage OS & ROOT包(可选)

3. 大致的流程
   1. 手机开机状态(打开USB调试),用ADB刷入TWRP-Recovery 或者手机fastboot状态(mi4-开机键+音量-)下,用Fastboot刷入TWRP-Recovery.
   
   2. 手机重启时进入TWRP-Recovery(mi4-开机键=音量+)或者手机重启后用ADB命令.
	`adb reboot recovery`

   3. 手机在TWRP-Recovery下双清wipe,之后用ADB命令写入卡刷包.   
	`adb push filename.zip /sdcard/`

		p.s.其实TWRP可以识别OTG的U盘,可以先把相关文件(recovery(*.img)、卡刷包(*.zip)、Root包(*.zip))前提U盘的读写速度可以，想想有些刷机包1点多G的...233

   4. 手机在TWRP-Recovery下install,刷入卡刷包，这时候也是可以继续刷入opengapps、root包的.
    
   5. 最后就可以重启手机了，开始新生！
   
4. 就这样开始吧！流量警告！！
  1. 开发者模式
  手机 设置>我的设备>全部参数>MiUI 版本(点击5次-开启开发者模式)

|![002-1-844190566787868161-设置-我的设备.png](/img/in-post/post-mi4tolineageos/002-1-844190566787868161-设置-我的设备.png)|![002-2-584811925639221627-我的设备-全部参数.png](/img/in-post/post-mi4tolineageos/002-2-584811925639221627-我的设备-全部参数.png)|![002-3-533915375131661992-全部参数-MIUI版本.png](/img/in-post/post-mi4tolineageos/002-3-533915375131661992-全部参数-MIUI版本.png)|



  2. USB调试
  手机 设置>更多设置>开发者选项>USB调试

|![002-1-844190566787868161-设置-我的设备.png](/img/in-post/post-mi4tolineageos/002-1-844190566787868161-设置-我的设备.png)|![002-4-280203510222175097-设置-更多设置.png](/img/in-post/post-mi4tolineageos/002-4-280203510222175097-设置-更多设置.png)|![002-5-69793988195590402-更多设置-开发者选项.png](/img/in-post/post-mi4tolineageos/002-5-69793988195590402-更多设置-开发者选项.png)|![002-6-20505554326648468-开发者选项.png](/img/in-post/post-mi4tolineageos/002-6-20505554326648468-开发者选项.png)|![002-7-559387598021082155-开发者选项-USB调试.png](/img/in-post/post-mi4tolineageos/002-7-559387598021082155-开发者选项-USB调试.png)|![002-8-110619712441753142-USB调试.png](/img/in-post/post-mi4tolineageos/002-8-110619712441753142-USB调试.png)| 

  3. 手机USB线连接PC,进入工具界面(cmd),(XX\MiFlash2018-5-28-0\Source\ThirdParty\Google\Android).

		p.s.最好是可以装一下手机的驱动.

  4. CMD界面,输入`adb devices`
     结果显示:`List of devices attached xxxxxxx device`

  5. 



 

TWRP

1. TWRP 3.2.1 汉化版 for cancro (Mi3/4)
[[软件] [5.1更新]TWRP 3.2.1-0 最新汉化版 For Cancro(MI 3/4) 含官方rec及教程](http://www.miui.com/thread-8369184-1-1.html)

## 后记