root@K2Plus-DBD5:~# hostname
K2Plus-DBD5
root@K2Plus-DBD5:~# uname -a
Linux K2Plus-DBD5 5.4.61 #1 SMP PREEMPT Tue Jun 23 09:45:29 CST 2026 armv7l GNU/Linux
root@K2Plus-DBD5:~# cat /etc/os-release
NAME="OpenWrt"
VERSION="21.02-SNAPSHOT"
ID="openwrt"
ID_LIKE="lede openwrt"
PRETTY_NAME="OpenWrt 21.02-SNAPSHOT"
VERSION_ID="21.02-snapshot"
HOME_URL="https://openwrt.org/"
BUG_URL="https://bugs.openwrt.org/"
SUPPORT_URL="https://forum.openwrt.org/"
BUILD_ID="r0-0b5de290a"
OPENWRT_BOARD="t113_i-CR0CN240110C10/generic"
OPENWRT_ARCH="arm_cortex-a7_neon"
OPENWRT_TAINTS="no-all glibc busybox"
OPENWRT_DEVICE_MANUFACTURER="OpenWrt"
OPENWRT_DEVICE_MANUFACTURER_URL="https://openwrt.org/"
OPENWRT_DEVICE_PRODUCT="Generic"
OPENWRT_DEVICE_REVISION="v0"
OPENWRT_RELEASE="OpenWrt 21.02-SNAPSHOT 5.0"
root@K2Plus-DBD5:~#

Filesystem                Size      Used Available Use% Mounted on
/dev/root               129.5M    129.5M         0 100% /rom
devtmpfs                234.9M         0    234.9M   0% /rom/dev
tmpfs                   244.1M      4.2M    239.9M   2% /tmp
/dev/mmcblk0p10         239.9M      7.9M    228.0M   3% /overlay
overlayfs:/overlay      239.9M      7.9M    228.0M   3% /
tmpfs                   512.0K         0    512.0K   0% /dev
/dev/by-name/UDISK       27.5G      4.3G     23.2G  16% /mnt/UDISK

root@K2Plus-DBD5:~# mount
/dev/root on /rom type squashfs (ro,relatime)
devtmpfs on /rom/dev type devtmpfs (rw,relatime,size=240520k,nr_inodes=60130,mode=755)
proc on /proc type proc (rw,nosuid,nodev,noexec,noatime)
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,noatime)
tmpfs on /tmp type tmpfs (rw,nosuid,nodev,noatime)
/dev/mmcblk0p10 on /overlay type ext4 (rw,noatime)
overlayfs:/overlay on / type overlay (rw,noatime,lowerdir=/,upperdir=/overlay/upper,workdir=/overlay/work)
tmpfs on /dev type tmpfs (rw,nosuid,relatime,size=512k,mode=755)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,mode=600,ptmxmode=000)
debugfs on /sys/kernel/debug type debugfs (rw,noatime)
none on /sys/kernel/config type configfs (rw,relatime)
adb on /dev/usb-ffs/adb type functionfs (rw,relatime)
/dev/by-name/UDISK on /mnt/UDISK type ext4 (rw,sync,relatime)


root@K2Plus-DBD5:~# ps -ef
PID   USER     TIME  COMMAND
    1 root      0:01 /sbin/procd
    2 root      0:00 [kthreadd]
    3 root      0:00 [rcu_gp]
    4 root      0:00 [rcu_par_gp]
    8 root      0:00 [mm_percpu_wq]
    9 root      1:01 [ksoftirqd/0]
   10 root      0:20 [rcu_preempt]
   11 root      0:01 [migration/0]
   12 root      0:00 [cpuhp/0]
   13 root      0:00 [cpuhp/1]
   14 root      0:00 [migration/1]
   15 root      0:05 [ksoftirqd/1]
   18 root      0:00 [kdevtmpfs]
   21 root      0:00 [rcu_tasks_kthre]
   34 root      0:04 [kworker/1:1-eve]
   35 root      0:01 [kworker/0:1-mm_]
  447 root      0:00 [oom_reaper]
  448 root      0:00 [writeback]
  483 root      0:00 [kblockd]
  621 root      0:18 [ion_system_heap]
  641 root      0:00 [watchdogd]
  736 root      0:00 [cfg80211]
  745 root      0:00 [kswapd0]
  847 root      0:00 [vsync proc 0]
  848 root      0:00 [vsync proc 1]
  941 root      0:00 [uas]
  986 root      0:00 [btudpwork]
  987 root      0:00 [btfwwork]
  997 root      1:21 [irq/42-mmc2]
 1001 root      0:00 [irq/43-mmc1]
 1013 root      0:00 [mmc_complete]
 1016 root      0:00 [3000008.dsp_rpr]
 1066 root      0:00 [ipv6_addrconf]
 1074 root      0:00 [krfcommd]
 1197 root      0:00 [jbd2/mmcblk0p10]
 1198 root      0:00 [ext4-rsv-conver]
 1348 ubus      0:00 /sbin/ubusd
 1355 root      0:00 /sbin/askfirst /bin/login
 1356 root      0:00 /sbin/askfirst /bin/login
 1569 root      0:00 /usr/bin/wipe_data
 1594 root      0:00 /usr/bin/dbus-daemon --system
 1706 logd      0:00 /sbin/logd -S 64
 1707 root      0:00 /sbin/logread -f -F /var/log/messages -p /var/run/logread.1.pid -S 512
 1728 root      0:01 [irq/227-usb_id]
 1849 root      0:00 /bin/adbd -D
 1902 root      0:00 /usr/sbin/ntpd -n -N -S /usr/sbin/ntpd-hotplug -p ntp5.aliyun.com -p 0.openwrt.pool.ntp.org -p 0.c
 1978 root      0:00 [kworker/0:3-ipv]
 2002 root      0:23 [dhd_watchdog_th]
 2003 root      2:41 [dhd_dpc]
 2004 root      0:30 [dhd_rxf]
 2014 root      0:00 [goodix_wq]
 2300 root      0:01 /sbin/netifd
 2625 root      0:45 [jbd2/mmcblk0p14]
 2626 root      0:00 [ext4-rsv-conver]
 2663 root      0:00 nginx: master process /usr/sbin/nginx -c /etc/nginx/nginx.conf -g daemon off;
 2704 nobody    0:23 nginx: worker process
 2735 root      0:00 /usr/bin/device_manager
 2779 root      0:59 /usr/bin/cam_app -i /dev/v4l/by-id/main-video0 -t 0 -w 1920 -h 1080 -f 15 -c
 2937 root      5:43 /usr/bin/webrtc_local
 2988 root      0:20 /usr/bin/mdns --service _Creality-8489732806DBD5._udp.local --port 5353 --hostname K2Plus-DBD5
 3126 root      0:28 /usr/bin/webrtc 8489732806DBD5 2
 3555 root     24:58 /usr/bin/master-server
 3556 root      1:38 /usr/bin/audio-server
 3557 root      0:07 /usr/bin/wifi-server
 3558 root      0:53 /usr/bin/app-server
 3561 root      0:02 /usr/bin/upgrade-server
 3562 root      1:04 /usr/bin/web-server
 3563 root      0:20 /usr/bin/Monitor
 3579 root      0:29 klipper_mcu -r
 3592 root     22:52 /usr/share/moonraker-env/bin/python /usr/share/moonraker/moonraker.py -c /usr/share/moonraker/moon
 3890 root      0:00 [dhd_eventd]
 3910 root     51:06 /usr/share/klippy-env/bin/python /usr/share/klipper/klippy/klippy.py /mnt/UDISK//printer_data/conf
 3913 root      0:01 wpa_supplicant -iwlan0 -Dnl80211 -c /etc/wifi/wpa_supplicant/wpa_supplicant.conf -m /etc/wifi/wpa_
 4031 root      2:07 /usr/bin/log_main
 4209 root     37:49 /usr/bin/display-server
 4258 root      0:00 /sbin/udhcpc -i wlan0 -S -t 5 -T 6 -b
 6533 root      0:01 [kworker/u4:5-ev]
10031 root      0:00 [kworker/1:0]
19370 root      0:01 [kworker/u5:1-uv]
21179 root      0:00 [kworker/1:1H-kb]
21181 root      0:01 [kworker/u5:2-uv]
21579 root      0:01 [kworker/u4:2-ev]
24237 root      0:01 [kworker/u4:1-ev]
25679 root      0:03 [kworker/u4:4-ev]
26194 root      0:01 [kworker/0:0H-mm]
28416 root      0:00 [kworker/u5:0-uv]
29549 root      0:00 /usr/sbin/dropbear -F -P /var/run/dropbear.1.pid -p 22 -K 300 -T 3
29892 root      0:00 [kworker/0:2H-mm]
30072 root      0:00 [kworker/u4:6-ev]
30328 root      0:00 [kworker/1:2H-kb]
30344 root      0:00 /usr/sbin/dropbear -F -P /var/run/dropbear.1.pid -p 22 -K 300 -T 3
30828 root      0:00 -ash
31230 root      0:00 [kworker/u5:3-uv]
32025 root      0:00 ps -ef

root@K2Plus-DBD5:~# netstat -tulpn
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 0.0.0.0:9999            0.0.0.0:*               LISTEN      3562/web-server
tcp        0      0 0.0.0.0:80              0.0.0.0:*               LISTEN      3562/web-server
tcp        0      0 0.0.0.0:7125            0.0.0.0:*               LISTEN      3592/python
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      30344/dropbear
tcp        0      0 0.0.0.0:4408            0.0.0.0:*               LISTEN      2663/nginx.conf -g
tcp        0      0 0.0.0.0:443             0.0.0.0:*               LISTEN      3562/web-server
tcp        0      0 0.0.0.0:8000            0.0.0.0:*               LISTEN      2937/webrtc_local
tcp        0      0 0.0.0.0:5037            0.0.0.0:*               LISTEN      1849/adbd
tcp        0      0 0.0.0.0:9998            0.0.0.0:*               LISTEN      3562/web-server
tcp        0      0 :::22                   :::*                    LISTEN      30344/dropbear
udp        0      0 0.0.0.0:5353            0.0.0.0:*                           2988/mdns
udp        0      0 :::5353                 :::*                                2988/mdns


ss -tulpn
