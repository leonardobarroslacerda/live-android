# Introduction #

config networking via console


# Commands #
## IP ##
ifconfig eth0 _yourip_ netmask _yourip's mask_

ifconfig eth0 192.168.1.10 netmask 255.255.255.0

not ipconfig!!!


## Gateway ##
route add default gw _yourgateway_ dev eth0

route add default gw 192.168.1.1 dev eth0


## DNS ##
setprop net.eth0.dns1 _yourDNS_

setprop net.eth0.dns1 208.67.222.222


## Proxy Server ##
Sorry, I find a way to config proxy
http://www.cnblogs.com/DesignPatterns/archive/2008/10/10/1307898.html.<br>
But it only be in effect when reboot machine. LiveAndroid save data in memory, after reboot, all<br>go back to initial setting. We'll change it soon.