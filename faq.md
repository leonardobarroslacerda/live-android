#FAQ collection

# FAQ #

last update: 2009-8-12



---

@stewart.midwinter

To join the two v.0.2 liveandroid .ISO files, you can use the COPY command in a command-prompt window: (similar commands exist for Mac OS X and Linux) **COPY /B liveandroidv0.2.iso.001 +liveandroidv0.2.iso.002 liveandroidv0.2.iso**

@liveandroid

thanks!


---

@spartango

Plz opensource method details? It be good to share build specifics so that things could be added & improved by others

@liveandroid

we'll publish the details on v1.0


---

@stewart.midwinter

Tried again in a Parallels virtual machine... When I run ifconfig specifying eth0 (sorry, not ipconfig!), I get an error message: ifconfig: SIOCSIFADDR no such device Looking in /system/etc/dhcpcd/dhcpcd.conf shows only a tiwlan0 interface. If I run ifconfig with this interface, I get the same error message. Looking the livedroid CD mentioned on the downloads page, the developer there does have networking working. If I type 'ifconfig' I get a response showing the eth0 interface. notice that in his boot sequence he runs a netcfg command. Hope this helps.

@dzo...@rambler.ru

# mkdir /data/misc/dhcp

# dhcpcd eth0


---

@recluze

I can't find the shortcut key to "Menu". Whenever an application comes up, there's no way of exiting it.

@liveandroid

Arrows(movement), Enter(confirm), Escape key(back), Alt + F1(console),Alt + F7(GUI)

http://s3.amazonaws.com/twitpic/photos/full/16550633.png?AWSAccessKeyId=0ZRYP5X5F6FSMBCCSE82&Expires=1247729880&Signature=H%2FUuxYoyuUfYselQPijt%2FlpYxpw%3D



---

@st.jingle

Hi, it can not boot on VirtualBox 3 on Debian testing AMD64

@MurzNN

It boots on Ubuntu Jaunty AMD64 with Virtualbox 3.0 normally, but for networking you need to select adapter **PCnet-FAST III** instead of default.


---

@mitcoes

How can be installed on a **pendrive** ?

@Apothh

For pendrive creation by terminal follow the next steps:

Install the required packages: syslinux, lilo (sudo apt-get install syslinux lilo)

Insert your pendrive with fat partition (!) in the next i call to /dev/sdb

Fix your MBR in the pen: sudo lilo -M /dev/sdb (not necessary)

Install syslinux bootloader to your partition: sudo syslinux -sf /dev/sdb1

Mount the liveandroid image: sudo mount -o loop <path to image> /cdrom

Mount your pendrive: sudo mount /dev/sdb1 /mnt

Copy the android files: sudo cp /cdrom/ /mnt

Sync the pendrive: sudo sync

Rename isolinux.cfg: sudo mv /mnt/isolinux.cfg /mnt/syslinux.cfg

Umount your pen: sudo umount /mnt


---

@MurzNN

Where is Android Market application? How I can install new applications?

@Apothh

I think, this is the android 1.5 sdk version, and this is not containing the market applicatin. But you can use google to find .apk files.


---

@ryoku\_cha

Failed to create a bootable @liveandroid USB-Stick. Tried with different Tools including UNetbootin, liveusb-creator and iso2usb

@liveandroid

we are fixing it now...


---

@Androidguide

If you won't get any further than the splashscreen, try increasing the Base Memory (e.g. to 200MB) and Video Memory (e.g. to 64MB). For most users, this works.

@liveandroid

thanks!


---

@recluze

I can't find the shortcut key to "Menu".

@cgarvey

The menu key is the Menu key on a Windows keyboard. It's the key (that usually is a logo of a drop down menu) to the right of the Windows key (with the Windows flag) to the right of the spacebar.



---

@Milan.Svoboda.G

Is it faster than simulator from SDK? Can I use live android to test and debug my application instead of using the simulator from SDK?

@liveandroid

sure. but liveandroid cannot replace SDK for debug purpose. if you want debug your apps, please install SDK.



---

@lucast1533

Using Parallels, it didn't work with "Other" as OS. Worked when I changed OS to "Linux" and "Other Linux"


---

@longshowliu

It's so greate, I just have a try ,but there is a problem ,how can I shut android down? just power off? Excuse a Noob.

@liveandroid

Alt+F1, /sbin/reboot -f now


---

@Androidguide

If you won't get any further than the splashscreen, try increasing the Base Memory (e.g. to 200MB) and Video Memory (e.g. to 64MB). For most users, this works.


---

@CyKiller

wifi works fine. If your using virtualization just use do NOT use the NAT settings and bridge your connection with the virtual settings. Hope it helps.


---

@dodo99x

Booted live 0.2 ISO perfectly under VirtualBox 3.0.0 [r49315](https://code.google.com/p/live-android/source/detail?r=49315). Used OS Type: Other/Unknown, 512mb ram, vt-x enabled, 128mb video memory, 4.77gb HD, Network PCnet-Fast III(NAT). Mouse, and keys work, internet too.


---

@lordsturm

Remember the G1 Android has 192MB of RAM, so it's essential you give it at least that much.


---

@diakopter

enable LiveAndroid 0.2 networking in VMWare Workstation 6.5:

  * Boot the LiveAndroid VM
  * Hit Alt-F1 to switch to the root console
  * mkdir /data/misc/dhcp
  * Stop the VM, and "Close" the VM in VMWare Workstation (or Exit VMWare Workstation)
  * Edit your VM's .vmx file so the "ethernet0.virtualDev" line reads: ethernet0.virtualDev = "vlance"
  * Open the .vmx file (launch the VM in VMWare)
  * Set the VM to have at least 384MB RAM
  * Start the VM; you're networked


---

@jonnymayne

using a xen virtual machine? My networking section in the config file reads: vif = 'type=ioemu, bridge=eth0, model=pcnet' eth0 appears under ifconfig after that.


---

@nathan.s...@gmail.com

If it hangs for you, see this bug: http://code.google.com/p/live-android/issues/detail?id=25