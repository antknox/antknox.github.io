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

  3. 准备文件:
 
   刷机工具 : MiFlash2018-5-28-0.zip [线刷工具- 通用刷机工具点击下载](http://bigota.d.miui.com/tools/MiFlash2018-5-28-0.zip)

   Recovery:
   
   TWRP: 

   原版 EN twrp-3.1.0-0-cancro.img [TWRP for cancro](https://dl.twrp.me/cancro/) 

   汉化版:[light]TWRP-3.2.1-0-cancro-zh_CN.img [下载](/files/2018-10/[light]TWRP-3.2.1-0-cancro-zh_CN.img) 

   by [[软件] [5.1更新]TWRP 3.2.1-0 最新汉化版 For Cancro(MI 3/4) 含官方rec及教程](http://www.miui.com/thread-8369184-1-1.html)

  卡刷包:

  Lineage OS : lineage-14.1-20181003-nightly-cancro-signed.zip [Builds for cancro](https://download.lineageos.org/cancro)
 
  ![003-2-2018-10-04_204936-mi4-lineageos-卡刷包.png](/img/in-post/post-mi4tolineageos/003-2-2018-10-04_204936-mi4-lineageos-卡刷包.png)

  相关:[在cancro上安装LineageOS-EN](https://wiki.lineageos.org/devices/cancro/install)

  su(root)包:addonsu-14.1-arm-signed.zip [Extras](https://download.lineageos.org/extras)

  ![003-3-2018-10-04_231354-extras-su(arm)-root包.png](/img/in-post/post-mi4tolineageos/003-3-2018-10-04_231354-extras-su(arm)-root包.png)

  Opengapps(谷歌全家桶) 

  [Google应用-EN](https://wiki.lineageos.org/gapps.html)

  [Opengapps](http://opengapps.org/?api=7.1&variant=nano)

  ![003-4-2018-10-05_205142-opengapps.png](/img/in-post/post-mi4tolineageos/003-4-2018-10-05_205142-opengapps.png)

  大合照:
  
  ![003-1-2018-10-04_214959-dir.png](/img/in-post/post-mi4tolineageos/003-1-2018-10-04_214959-dir.png)

  3. 手机开机状态用USB线连接PC,
 
   进入工具界面(cmd),(XX\MiFlash2018-5-28-0\Source\ThirdParty\Google\Android).

   ![004-1-2018-10-04_205937-cmd.png](/img/in-post/post-mi4tolineageos/004-1-2018-10-04_205937-cmd.png)

   p.s.最好是可以装一下手机的驱动,手机有锁的先解锁,重要的数据记得备份!!!

  4. 检测设备,是否连接上手机.

   CMD界面,

   输入`adb devices`

   结果显示:`List of devices attached xxxxxxx device`

   ![004-2-2018-10-04_205955-cmd-adb-devices.png](/img/in-post/post-mi4tolineageos/004-2-2018-10-04_205955-cmd-adb-devices.png)


  5. 让手机重启进入Fastboot模式.

  CMD界面,

  输入`adb reboot bootloader`

  ![004-3-2018-10-04_233458-adb-reboot-bootloader-fastboot.png](/img/in-post/post-mi4tolineageos/004-3-2018-10-04_233458-adb-reboot-bootloader-fastboot.png)

  手机重启后,就会进入Fastboot,出现下面的界面.

  ![004-4-IMG_20181004_210658-fastboot.jpg](/img/in-post/post-mi4tolineageos/004-4-IMG_20181004_210658-fastboot.jpg)

  6. 开始刷入TWRP的Recovery.

   先检测电脑是否连接上手机.

   CMD界面,

   输入`fastboot devices`

   结果显示:`xxxxxxx fastboot`

   ![004-5-2018-10-04_210732-fastboot-devices.png](/img/in-post/post-mi4tolineageos/004-5-2018-10-04_210732-fastboot-devices.png)

   开始刷入Recovery.

   CMD界面,

   输入`fastboot flash recovery files.img` (注意img文件的路径)

   ![004-6-2018-10-04_210847-fastboot-flash-recovery.png](/img/in-post/post-mi4tolineageos/004-6-2018-10-04_210847-fastboot-flash-recovery.png)

  7. 刷入Recovery后,重启手机.
  
   CMD界面,

   输入`Fastboot reboot`
   
   重启手机.

  ![004-7-2018-10-04_211044-fastboot-reboot.png](/img/in-post/post-mi4tolineageos/004-7-2018-10-04_211044-fastboot-reboot.png)

   手机开始重启
   
   ![004-8-IMG_20181004_211522-mi.jpg](/img/in-post/post-mi4tolineageos/004-8-IMG_20181004_211522-mi.jpg)

  8. 手机重启完后,开始进入Recovery操作.
  
   CMD界面,

   输入`adb devices`

   确认连接上手机.

   输入`adb reboot recovery`

   手机重启进入Recovery.

   ![004-9-2018-10-04_211647-adb-reboot-recovery.png](/img/in-post/post-mi4tolineageos/004-9-2018-10-04_211647-adb-reboot-recovery.png)

   TWRP界面

   ![004-10-IMG_20181004_211526-twrp.jpg](/img/in-post/post-mi4tolineageos/004-10-IMG_20181004_211526-twrp.jpg)

   TWRP操作界面

   ![004-11-2018-10-4-_000000-twrp.png](/img/in-post/post-mi4tolineageos/004-11-2018-10-4-_000000-twrp.png) 

   如果文字显示的不是中文的话,可以在设置那里修改.

   ![004-12-IMG_20181004_211933-lng.jpg](/img/in-post/post-mi4tolineageos/004-12-IMG_20181004_211933-lng.jpg)

   TWRP 界面 点击 清除(WIPE) (不同的系统,版本,都需要双清(删除数据))

   ![004-12-IMG_20181004_211531-界面.jpg](/img/in-post/post-mi4tolineageos/004-13-IMG_20181004_211531-界面.jpg)

   清除(WIPE)界面 (一般就直接双清就可以了,如果想把手机的内置的sdcard(机身内置储存)的全部文件删除,可以按下面的操作.)

   ![004-14-IMG_20181004_211539-wipe-双清.jpg](/img/in-post/post-mi4tolineageos/004-14-IMG_20181004_211539-wipe-双清.jpg)

   (如果不需要全部清除输出的话,请跳过!) 格式化手机内置sdcard. 点击 格式化DATA分区, 就会出现下面的界面.

   ![004-15-IMG_20181004_211903-format-data.jpg](/img/in-post/post-mi4tolineageos/004-15-IMG_20181004_211903-format-data.jpg)

   (如果不需要全部清除输出的话,请跳过!) 格式化手机内置sdcard. 输入 yes 回车 确认操作.

   ![004-16-IMG_20181004_211917-format-data-yes.jpg](/img/in-post/post-mi4tolineageos/004-16-IMG_20181004_211917-format-data-yes.jpg)

  9. 开始写入卡刷包到手机内置sdcard (DATA分区)
  
   CMD界面,

   输入`adb devices`

   确认连接上手机.

   ![005-1-2018-10-04_210212-adb-devices.png](/img/in-post/post-mi4tolineageos/005-1-2018-10-04_210212-adb-devices.png)

   输入`adb push files.zip /sdcard/` (注意zip文件的路径)

   写入卡刷包.

   ![005-2-2018-10-04_211740-adb-push-1.png](/img/in-post/post-mi4tolineageos/005-2-2018-10-04_211740-adb-push-1.png)

   写入完成.

   ![005-3-2018-10-04_211812-adb-push-2.png](/img/in-post/post-mi4tolineageos/005-3-2018-10-04_211812-adb-push-2.png)

  10. 返回主界面,开始在TWRP上刷入Lineage OS
   
   TWRP界面

   ![004-13-IMG_20181004_211531-界面.jpg](/img/in-post/post-mi4tolineageos/004-13-IMG_20181004_211531-界面.jpg)

   点击 安装(install) 界面如下.

   ![005-4-IMG_20181004_211546-install.jpg](/img/in-post/post-mi4tolineageos/005-4-IMG_20181004_211546-install.jpg).

   其实,TWRP也是可以识别OTG的.

   ![005-5-IMG_20181004_220058-OTG-U.jpg](/img/in-post/post-mi4tolineageos/005-5-IMG_20181004_220058-OTG-U.jpg)

   ![005-6-IMG_20181004_220106-OTG-U-files.jpg](/img/in-post/post-mi4tolineageos/005-6-IMG_20181004_220106-OTG-U-files.jpg)

   安装(install)界面,选择卡刷包 lineage-14.1-20181003-nightly-cancro-signed.zip

   ![005-8-IMG_20181004_211832-install-选择卡刷包-2.jpg](/img/in-post/post-mi4tolineageos/005-8-IMG_20181004_211832-install-选择卡刷包-2.jpg)

   滑动下方箭头,确认刷入.(按照这样的方法,可以刷入su(root)包或者opengapps包)

   ![005-9-IMG_20181004_211841-刷入卡刷包.jpg](/img/in-post/post-mi4tolineageos/005-9-IMG_20181004_211841-刷入卡刷包.jpg)

   刷入完成后.REBOOT SYSTEM

   ![005-10-IMG_20181004_211958-reboot.jpg](/img/in-post/post-mi4tolineageos/005-10-IMG_20181004_211958-reboot.jpg)

  11. LIneage OS 登场.

   ![006-1-IMG_20181004_211433-lineageos-1.jpg](/img/in-post/post-mi4tolineageos/006-1-IMG_20181004_211433-lineageos-1.jpg)

   ![006-2-IMG_20181004_211053-lineageos-2.jpg](/img/in-post/post-mi4tolineageos/006-2-IMG_20181004_211053-lineageos-2.jpg)

   ![006-3-IMG_20181004_211101-lineageos-3.jpg](/img/in-post/post-mi4tolineageos/006-3-IMG_20181004_211101-lineageos-3.jpg)

   ![006-4-IMG_20181004_211111-lineageos.jpg](/img/in-post/post-mi4tolineageos/006-4-IMG_20181004_211111-lineageos.jpg)


## 后记

   最后,安装`黑域`,启动`隐私防护`,还有`系统情景`超级好用.

   还有 Tasker,adb工具安装器(网络).