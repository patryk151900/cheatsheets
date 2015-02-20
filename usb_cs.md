http://hanneton.org/blog/hacking-the-kyoto-heart-rate-monitor-2901/
https://securfox.wordpress.com/2009/11/15/sniffing-usb-port-on-linux/

mount debugfs
mount -t debugfs none_debugs /sys/kernel/debug

run usbmon module
modprobe usbmon

check if usbmon is running
lsmod | grep usbmod

list all usb debug nodes
sudo ls /sys/kernel/debug/usb/usbmon

0 are hub, 1x are devices

check which device do you want to watch
lsusb		#the order is later 1s 1t 1u ...
lsusb -v	#verbose mode

cat certain device
/sys/kernel/debug/usb/usbmon/1u

with use of tcpdump
tcpdump -D		#list of devices
tcpdump -i usbmon1 -w /data/usblog.pcap &
