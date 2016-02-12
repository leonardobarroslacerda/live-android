please follow & RT, http://twitter.com/liveandroid


# Introduction #

HOWTO use live-android


# Download & Boot #

**liveandroid v0.1**

1. Download androidv0.1.part1.rar/androidv0.1.part2.rar/androidv0.1.part3.rar, unzip it. you'll get androidv0.1.iso

Now, you can download liveandroidv0.1.iso directly from rapidshare -> http://rapidshare.com/files/249259326/liveandroidv0.1.iso

thanks mirror:
http://g-android.com/liveandroid/androidv0.1.iso <- hosting in Vietnam
http://tomcode.com/inside/live-android/androidv0.1.iso

2. use androidv0.1.iso in vmware or virtualbox to your taste. of cource, you can burn it as a LiveCD.

3. boot and enjoy!


**liveandroid v0.2**

### [LiveCD ](.md) ###

1. Download liveandroidv0.2.iso.001/liveandroidv0.2.iso.002

  * windows, use HJSplit(http://www.freebyte.com/hjsplit/ or http://www.freebytesoftware.com/download/hjsplit.zip) to join it. also use command COPY /B liveandroidv0.2.iso.001 + liveandroidv0.2.iso.002 liveandroidv0.2.iso

  * linux, cat liveandroidv0.2.iso.001 liveandroidv0.2.iso.002 > liveandroidv0.2.iso

2. Check md5sum via http://www.pc-tools.net/win32/md5sums/ or http://www.pc-tools.net/files/win32/freeware/md5sums-1.2.zip

**liveandroidv0.2.iso MD5: 03852bce8cb26aba21d147153c1fb120**

3. use liveandroidv0.2.iso in vmware or virtualbox to your taste. of cource, you can burn it as a LiveCD.

4. boot and enjoy!

### [LiveUSB ](.md) ###

1. Download liveandroidv0.2usb.iso.001/liveandroidv0.2usb.iso.002

  * windows, use HJSplit(http://www.freebyte.com/hjsplit/ or http://www.freebytesoftware.com/download/hjsplit.zip) to join it. also use command COPY /B liveandroidv0.2usb.iso.001 + liveandroidv0.2usb.iso.002 liveandroidv0.2usb.iso

  * linux, cat liveandroidv0.2usb.iso.001 liveandroidv0.2usb.iso.002 > liveandroidv0.2usb.iso

2. Check md5sum via http://www.pc-tools.net/win32/md5sums/ or http://www.pc-tools.net/files/win32/freeware/md5sums-1.2.zip

**liveandroidv0.2usb.iso MD5: 15e39e524e15a407185ade97ba648df6**

3. use liveandroidv0.2usb.iso in vmware or virtualbox to your taste. of cource, you can use UNetbootin(http://unetbootin.sourceforge.net) to make it as a LiveUSB.

4. boot and enjoy!


# Tips #

use **alt+F1** or **alt+F7** to switch GUI and console.

busybox added, you can do everything in console.

play with HOME Key and MENU key
![http://web5.twitpic.com/img/16550633-abc16511dbecf5489fe46b035aaa138c.4a56aeb7-full.png](http://web5.twitpic.com/img/16550633-abc16511dbecf5489fe46b035aaa138c.4a56aeb7-full.png)


# Networking #

liveandroidv0.2.iso support DHCP, if you want to configure in console, press alt+F1, then

**IP**

ifconfig eth0 _yourip_ netmask _yourip's mask_

e.g. ifconfig eth0 192.168.1.10 netmask 255.255.255.0

**Gateway**

route add default gw _yourgateway_ dev eth0

e.g. route add default gw 192.168.1.1 dev eth0


**DNS**

setprop net.eth0.dns1 _yourDNS_

e.g. setprop net.eth0.dns1 208.67.222.222