The laggy bluetooth mouse problem is a know issue and you can use the following workaround:

(Taken from https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1824559/comments/10 and https://bbs.archlinux.org/viewtopic.php?pid=1857256):

`sudo nano /var/lib/bluetooth/xx:xx:xx:xx:xx:xx/yy:yy:yy:yy:yy:yy/info`

where xx:xx:xx:xx:xx:xx is the address of your Bluetooth adapter and yy:yy:yy:yy:yy:yy is address of your Bluetooth mouse. Add the following lines to this file and save your changes:

[ConnectionParameters]
MinInterval=6
MaxInterval=7
Latency=0
Timeout=216
Then restart your Bluetooth service:

`sudo systemctl restart bluetooth`

This solution also works after rebooting your system.