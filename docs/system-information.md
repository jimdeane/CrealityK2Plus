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


root@K2Plus-DBD5:~# find / -name "printer.cfg" 2>/dev/null
/mnt/UDISK/printer_data/config/printer.cfg
/rom/usr/share/klipper/config/F008/printer.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/printer.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13_1/printer.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/printer.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/printer.cfg
/rom/usr/share/klipper/config/GS_01_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/printer.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/K1C_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S10/printer.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S11/printer.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR0CN240110C10/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S11/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/PF027_CR0CN250701C10/printer.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/F008/printer.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/printer.cfg
/usr/share/klipper/config/F008_CR0CN240319C13_1/printer.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/printer.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/printer.cfg
/usr/share/klipper/config/GS_01_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/printer.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/K1C_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/K1_CR4CU220812S10/printer.cfg
/usr/share/klipper/config/K1_CR4CU220812S11/printer.cfg
/usr/share/klipper/config/K1_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/K1_MAX_CR0CN240110C10/printer.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S11/printer.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/PF027_CR0CN250701C10/printer.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/printer.cfg


root@K2Plus-DBD5:~# find / -name "*.cfg" 2>/dev/null
/bin/mtop.cfg
/etc/rc_maps.cfg
/etc/recorder.cfg
/mnt/UDISK/printer_data/config/printer-20260714_101142.cfg
/mnt/UDISK/printer_data/config/printer-20260713_054054.cfg
/mnt/UDISK/printer_data/config/printer-20260714_094421.cfg
/mnt/UDISK/printer_data/config/printer-20260713_052102.cfg
/mnt/UDISK/printer_data/config/printer-20260714_085347.cfg
/mnt/UDISK/printer_data/config/printer-20260714_133356.cfg
/mnt/UDISK/printer_data/config/printer-20260715_084443.cfg
/mnt/UDISK/printer_data/config/printer.cfg
/mnt/UDISK/printer_data/config/box.cfg
/mnt/UDISK/printer_data/config/printer-20260713_053015.cfg
/mnt/UDISK/printer_data/config/printer-20260713_070832.cfg
/mnt/UDISK/printer_data/config/printer-20260713_052519.cfg
/mnt/UDISK/printer_data/config/printer-20260713_053016.cfg
/mnt/UDISK/printer_data/config/sensorless.cfg
/mnt/UDISK/printer_data/config/motor_control.cfg
/mnt/UDISK/printer_data/config/printer_params.cfg
/mnt/UDISK/printer_data/config/gcode_macro.cfg
/mnt/UDISK/printer_data/config/printer-20260714_121728.cfg
/rom/bin/mtop.cfg
/rom/etc/rc_maps.cfg
/rom/etc/recorder.cfg
/rom/usr/lib/python3.9/site-packages/pip/_vendor/distlib/_backport/sysconfig.cfg
/rom/usr/lib/python3.9/site-packages/pycparser/_c_ast.cfg
/rom/usr/lib/python3.9/site-packages/tornado/test/options_test.cfg
/rom/usr/lib/python3.9/site-packages/tornado/test/options_test_types.cfg
/rom/usr/lib/python3.9/site-packages/tornado/test/options_test_types_str.cfg
/rom/usr/share/klipper/config/F008/box.cfg
/rom/usr/share/klipper/config/F008/factory_printer.cfg
/rom/usr/share/klipper/config/F008/gcode_macro.cfg
/rom/usr/share/klipper/config/F008/printer.cfg
/rom/usr/share/klipper/config/F008/printer_params.cfg
/rom/usr/share/klipper/config/F008/sensorless.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/box.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/factory_printer.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/gcode_macro.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/motor_control.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/printer.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/printer_params.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13/sensorless.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13_1/box.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13_1/factory_printer.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13_1/gcode_macro.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13_1/printer.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13_1/printer_params.cfg
/rom/usr/share/klipper/config/F008_CR0CN240319C13_1/sensorless.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/box.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/factory_printer.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/gcode_macro.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/motor_control.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/printer_params.cfg
/rom/usr/share/klipper/config/F012_CR0CN200400C10/sensorless.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/box.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/factory_printer.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/gcode_macro.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/motor_control.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/printer_params.cfg
/rom/usr/share/klipper/config/F021_CR0CN200400C10/sensorless.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/box.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/factory_printer.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/gcode_macro.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/motor_control.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/printer_params.cfg
/rom/usr/share/klipper/config/F025_CR0CN200400C10/sensorless.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/box.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/factory_printer.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/gcode_macro.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/motor_control.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/printer.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/printer_params.cfg
/rom/usr/share/klipper/config/F037_CR5NN251101C10/sensorless.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/box.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/factory_printer.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/gcode_macro.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/motor_control.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/printer.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/printer_params.cfg
/rom/usr/share/klipper/config/F038_CR4SNF038C01/sensorless.cfg
/rom/usr/share/klipper/config/GS_01_CR4CU220812S12/factory_printer.cfg
/rom/usr/share/klipper/config/GS_01_CR4CU220812S12/gcode_macro.cfg
/rom/usr/share/klipper/config/GS_01_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/GS_01_CR4CU220812S12/printer_params.cfg
/rom/usr/share/klipper/config/GS_01_CR4CU220812S12/sensorless.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/box.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/factory_printer.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/gcode_macro.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/motor_control.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/printer.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/printer_params.cfg
/rom/usr/share/klipper/config/GS_03_CR0CN240319C13/sensorless.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/box.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/factory_printer.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/gcode_macro.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/motor_control.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/printer_params.cfg
/rom/usr/share/klipper/config/GS_04_CR0CN200400C10/sensorless.cfg
/rom/usr/share/klipper/config/K1C_CR4CU220812S12/factory_printer.cfg
/rom/usr/share/klipper/config/K1C_CR4CU220812S12/gcode_macro.cfg
/rom/usr/share/klipper/config/K1C_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/K1C_CR4CU220812S12/printer_params.cfg
/rom/usr/share/klipper/config/K1C_CR4CU220812S12/sensorless.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S10/gcode_macro.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S10/printer.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S10/printer_params.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S10/sensorless.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S11/gcode_macro.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S11/printer.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S11/printer_params.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S11/sensorless.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S12/factory_printer.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S12/gcode_macro.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S12/printer_params.cfg
/rom/usr/share/klipper/config/K1_CR4CU220812S12/sensorless.cfg
/rom/usr/share/klipper/config/K1_MAX_CR0CN240110C10/factory_printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR0CN240110C10/gcode_macro.cfg
/rom/usr/share/klipper/config/K1_MAX_CR0CN240110C10/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR0CN240110C10/printer_params.cfg
/rom/usr/share/klipper/config/K1_MAX_CR0CN240110C10/sensorless.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S11/gcode_macro.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S11/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S11/printer_params.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S11/sensorless.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S12/box.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S12/factory_printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S12/gcode_macro.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S12/printer_params.cfg
/rom/usr/share/klipper/config/K1_MAX_CR4CU220812S12/sensorless.cfg
/rom/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/factory_printer.cfg
/rom/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/gcode_macro.cfg
/rom/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/printer.cfg
/rom/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/printer_params.cfg
/rom/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/sensorless.cfg
/rom/usr/share/klipper/config/PF027_CR0CN250701C10/box.cfg
/rom/usr/share/klipper/config/PF027_CR0CN250701C10/factory_printer.cfg
/rom/usr/share/klipper/config/PF027_CR0CN250701C10/gcode_macro.cfg
/rom/usr/share/klipper/config/PF027_CR0CN250701C10/printer.cfg
/rom/usr/share/klipper/config/PF027_CR0CN250701C10/printer_params.cfg
/rom/usr/share/klipper/config/PF027_CR0CN250701C10/sensorless.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/box.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/factory_printer.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/gcode_macro.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/motor_control.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/printer.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/printer_params.cfg
/rom/usr/share/klipper/config/Z2_CR0CN200400C10/sensorless.cfg
/rom/usr/share/klipper/config/example-cartesian.cfg
/rom/usr/share/klipper/config/example-corexy.cfg
/rom/usr/share/klipper/config/example-corexz.cfg
/rom/usr/share/klipper/config/example-delta.cfg
/rom/usr/share/klipper/config/example-deltesian.cfg
/rom/usr/share/klipper/config/example-extras.cfg
/rom/usr/share/klipper/config/example-hybrid-corexy.cfg
/rom/usr/share/klipper/config/example-hybrid-corexz.cfg
/rom/usr/share/klipper/config/example-polar.cfg
/rom/usr/share/klipper/config/example-rotary-delta.cfg
/rom/usr/share/klipper/config/example-winch.cfg
/rom/usr/share/klipper/config/example.cfg
/rom/usr/share/klipper/config/generic-alligator-r2.cfg
/rom/usr/share/klipper/config/generic-alligator-r3.cfg
/rom/usr/share/klipper/config/generic-archim2.cfg
/rom/usr/share/klipper/config/generic-azteeg-x5-mini-v3.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-e3-rrf-v1.1.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-gtr.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-manta-m4p.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-manta-m8p.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-octopus.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-2.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-3.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-cr6-v1.0.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-e3-dip.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-e3-turbo.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v1.0.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v1.2.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v2.0.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v3.0.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-mini-mz.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-mini.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-pico-v1.0.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-pro.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-v1.1.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-v1.3.cfg
/rom/usr/share/klipper/config/generic-bigtreetech-skr-v1.4.cfg
/rom/usr/share/klipper/config/generic-cramps.cfg
/rom/usr/share/klipper/config/generic-creality-v4.2.10.cfg
/rom/usr/share/klipper/config/generic-creality-v4.2.7.cfg
/rom/usr/share/klipper/config/generic-duet2-duex.cfg
/rom/usr/share/klipper/config/generic-duet2-maestro.cfg
/rom/usr/share/klipper/config/generic-duet2.cfg
/rom/usr/share/klipper/config/generic-duet3-mini.cfg
/rom/usr/share/klipper/config/generic-einsy-rambo.cfg
/rom/usr/share/klipper/config/generic-flyboard.cfg
/rom/usr/share/klipper/config/generic-fysetc-cheetah-v1.1.cfg
/rom/usr/share/klipper/config/generic-fysetc-cheetah-v1.2.cfg
/rom/usr/share/klipper/config/generic-fysetc-f6.cfg
/rom/usr/share/klipper/config/generic-fysetc-s6-v2.cfg
/rom/usr/share/klipper/config/generic-fysetc-s6.cfg
/rom/usr/share/klipper/config/generic-fysetc-spider.cfg
/rom/usr/share/klipper/config/generic-gt2560.cfg
/rom/usr/share/klipper/config/generic-mellow-fly-cdy-v3.cfg
/rom/usr/share/klipper/config/generic-mellow-fly-gemini-v1.cfg
/rom/usr/share/klipper/config/generic-mellow-fly-gemini-v2.cfg
/rom/usr/share/klipper/config/generic-mellow-super-infinty-hv.cfg
/rom/usr/share/klipper/config/generic-melzi.cfg
/rom/usr/share/klipper/config/generic-mightyboard.cfg
/rom/usr/share/klipper/config/generic-mini-rambo.cfg
/rom/usr/share/klipper/config/generic-minitronics1.cfg
/rom/usr/share/klipper/config/generic-mks-robin-e3.cfg
/rom/usr/share/klipper/config/generic-mks-robin-nano-v1.cfg
/rom/usr/share/klipper/config/generic-mks-robin-nano-v2.cfg
/rom/usr/share/klipper/config/generic-mks-robin-nano-v3.cfg
/rom/usr/share/klipper/config/generic-mks-rumba32-v1.0.cfg
/rom/usr/share/klipper/config/generic-mks-sgenl.cfg
/rom/usr/share/klipper/config/generic-printrboard-g2.cfg
/rom/usr/share/klipper/config/generic-printrboard.cfg
/rom/usr/share/klipper/config/generic-prusa-buddy.cfg
/rom/usr/share/klipper/config/generic-radds.cfg
/rom/usr/share/klipper/config/generic-rambo.cfg
/rom/usr/share/klipper/config/generic-ramps.cfg
/rom/usr/share/klipper/config/generic-re-arm.cfg
/rom/usr/share/klipper/config/generic-replicape.cfg
/rom/usr/share/klipper/config/generic-rumba.cfg
/rom/usr/share/klipper/config/generic-ruramps-v1.3.cfg
/rom/usr/share/klipper/config/generic-simulavr.cfg
/rom/usr/share/klipper/config/generic-smoothieboard.cfg
/rom/usr/share/klipper/config/generic-th3d-ezboard-lite-v1.2.cfg
/rom/usr/share/klipper/config/generic-th3d-ezboard-lite-v2.0.cfg
/rom/usr/share/klipper/config/generic-ultimaker-ultimainboard-v2.cfg
/rom/usr/share/klipper/config/kit-voron2-250mm.cfg
/rom/usr/share/klipper/config/kit-zav3d-2019.cfg
/rom/usr/share/klipper/config/printer-adimlab-2018.cfg
/rom/usr/share/klipper/config/printer-alfawise-u30-2018.cfg
/rom/usr/share/klipper/config/printer-anet-a4-2018.cfg
/rom/usr/share/klipper/config/printer-anet-a8-2017.cfg
/rom/usr/share/klipper/config/printer-anet-a8-2019.cfg
/rom/usr/share/klipper/config/printer-anet-e10-2018.cfg
/rom/usr/share/klipper/config/printer-anet-e16-2019.cfg
/rom/usr/share/klipper/config/printer-anycubic-4max-2018.cfg
/rom/usr/share/klipper/config/printer-anycubic-4maxpro-2.0-2021.cfg
/rom/usr/share/klipper/config/printer-anycubic-i3-mega-2017.cfg
/rom/usr/share/klipper/config/printer-anycubic-kossel-2016.cfg
/rom/usr/share/klipper/config/printer-anycubic-kossel-plus-2017.cfg
/rom/usr/share/klipper/config/printer-anycubic-vyper-2021.cfg
/rom/usr/share/klipper/config/printer-artillery-sidewinder-x2-2022.cfg
/rom/usr/share/klipper/config/printer-biqu-b1-se-plus-2022.cfg
/rom/usr/share/klipper/config/printer-biqu-bx-2021.cfg
/rom/usr/share/klipper/config/printer-bq-hephestos-2014.cfg
/rom/usr/share/klipper/config/printer-creality-cr10-2017.cfg
/rom/usr/share/klipper/config/printer-creality-cr10-smart-pro-2022.cfg
/rom/usr/share/klipper/config/printer-creality-cr10-v3-2020.cfg
/rom/usr/share/klipper/config/printer-creality-cr10mini-2017.cfg
/rom/usr/share/klipper/config/printer-creality-cr10s-2017.cfg
/rom/usr/share/klipper/config/printer-creality-cr20-2018.cfg
/rom/usr/share/klipper/config/printer-creality-cr20-pro-2019.cfg
/rom/usr/share/klipper/config/printer-creality-cr30-2021.cfg
/rom/usr/share/klipper/config/printer-creality-cr6se-2020.cfg
/rom/usr/share/klipper/config/printer-creality-cr6se-2021.cfg
/rom/usr/share/klipper/config/printer-creality-ender2-2017.cfg
/rom/usr/share/klipper/config/printer-creality-ender2pro-2021.cfg
/rom/usr/share/klipper/config/printer-creality-ender3-2018.cfg
/rom/usr/share/klipper/config/printer-creality-ender3-s1-2021.cfg
/rom/usr/share/klipper/config/printer-creality-ender3-s1plus-2022.cfg
/rom/usr/share/klipper/config/printer-creality-ender3-v2-2020.cfg
/rom/usr/share/klipper/config/printer-creality-ender3max-2021.cfg
/rom/usr/share/klipper/config/printer-creality-ender3pro-2020.cfg
/rom/usr/share/klipper/config/printer-creality-ender5-2019.cfg
/rom/usr/share/klipper/config/printer-creality-ender5plus-2019.cfg
/rom/usr/share/klipper/config/printer-creality-ender5pro-2020.cfg
/rom/usr/share/klipper/config/printer-creality-ender6-2020.cfg
/rom/usr/share/klipper/config/printer-creality-sermoonD1-2021.cfg
/rom/usr/share/klipper/config/printer-creality-sermoonV1-2022.cfg
/rom/usr/share/klipper/config/printer-elegoo-neptune2-2021.cfg
/rom/usr/share/klipper/config/printer-eryone-er20-2021.cfg
/rom/usr/share/klipper/config/printer-eryone-thinker-series-v2-2020.cfg
/rom/usr/share/klipper/config/printer-flashforge-creator-pro-2018.cfg
/rom/usr/share/klipper/config/printer-flsun-q5-2020.cfg
/rom/usr/share/klipper/config/printer-flsun-qqs-2020.cfg
/rom/usr/share/klipper/config/printer-fokoos-odin5-f3-2021.cfg
/rom/usr/share/klipper/config/printer-geeetech-301-2019.cfg
/rom/usr/share/klipper/config/printer-hiprecy-leo-2019.cfg
/rom/usr/share/klipper/config/printer-longer-lk4-pro-2019.cfg
/rom/usr/share/klipper/config/printer-lulzbot-mini1-2016.cfg
/rom/usr/share/klipper/config/printer-lulzbot-taz6-2017.cfg
/rom/usr/share/klipper/config/printer-lulzbot-taz6-dual-v3-2017.cfg
/rom/usr/share/klipper/config/printer-makergear-m2-2012.cfg
/rom/usr/share/klipper/config/printer-makergear-m2-2016.cfg
/rom/usr/share/klipper/config/printer-micromake-d1-2016.cfg
/rom/usr/share/klipper/config/printer-modix-big60-2020.cfg
/rom/usr/share/klipper/config/printer-monoprice-mini-delta-2017.cfg
/rom/usr/share/klipper/config/printer-monoprice-select-mini-v1-2016.cfg
/rom/usr/share/klipper/config/printer-monoprice-select-mini-v2-2018.cfg
/rom/usr/share/klipper/config/printer-mtw-create-2015.cfg
/rom/usr/share/klipper/config/printer-prusa-mini-plus-2020.cfg
/rom/usr/share/klipper/config/printer-robo3d-r2-2017.cfg
/rom/usr/share/klipper/config/printer-seemecnc-rostock-max-v2-2015.cfg
/rom/usr/share/klipper/config/printer-sovol-sv01-2020.cfg
/rom/usr/share/klipper/config/printer-sunlu-s8-2020.cfg
/rom/usr/share/klipper/config/printer-tevo-flash-2018.cfg
/rom/usr/share/klipper/config/printer-tevo-tarantula-pro-2020.cfg
/rom/usr/share/klipper/config/printer-tronxy-p802e-2020.cfg
/rom/usr/share/klipper/config/printer-tronxy-p802m-2020.cfg
/rom/usr/share/klipper/config/printer-tronxy-x5s-2018.cfg
/rom/usr/share/klipper/config/printer-tronxy-x5sa-pro-2020.cfg
/rom/usr/share/klipper/config/printer-tronxy-x5sa-v6-2019.cfg
/rom/usr/share/klipper/config/printer-tronxy-x8-2018.cfg
/rom/usr/share/klipper/config/printer-tronxy-xy-2-Pro-2020.cfg
/rom/usr/share/klipper/config/printer-twotrees-sapphire-plus-sp-5-v1-2020.cfg
/rom/usr/share/klipper/config/printer-twotrees-sapphire-plus-sp-5-v1.1-2021.cfg
/rom/usr/share/klipper/config/printer-twotrees-sapphire-pro-sp-3-2020.cfg
/rom/usr/share/klipper/config/printer-velleman-k8200-2013.cfg
/rom/usr/share/klipper/config/printer-velleman-k8800-2017.cfg
/rom/usr/share/klipper/config/printer-wanhao-duplicator-6-2016.cfg
/rom/usr/share/klipper/config/printer-wanhao-duplicator-9-2018.cfg
/rom/usr/share/klipper/config/printer-wanhao-duplicator-i3-mini-2017.cfg
/rom/usr/share/klipper/config/printer-wanhao-duplicator-i3-plus-2017.cfg
/rom/usr/share/klipper/config/printer-wanhao-duplicator-i3-plus-mark2-2019.cfg
/rom/usr/share/klipper/config/printer-wanhao-duplicator-i3-v2.1-2017.cfg
/rom/usr/share/klipper/config/sample-aliases.cfg
/rom/usr/share/klipper/config/sample-bigtreetech-ebb-canbus-v1.0.cfg
/rom/usr/share/klipper/config/sample-bigtreetech-ebb-canbus-v1.1.cfg
/rom/usr/share/klipper/config/sample-bigtreetech-exp-mot.cfg
/rom/usr/share/klipper/config/sample-bigtreetech-hermit-crab-canbus.cfg
/rom/usr/share/klipper/config/sample-glyphs.cfg
/rom/usr/share/klipper/config/sample-huvud-v0.61.cfg
/rom/usr/share/klipper/config/sample-idex.cfg
/rom/usr/share/klipper/config/sample-lcd.cfg
/rom/usr/share/klipper/config/sample-macros.cfg
/rom/usr/share/klipper/config/sample-mmu2s-diy.cfg
/rom/usr/share/klipper/config/sample-multi-extruder.cfg
/rom/usr/share/klipper/config/sample-multi-mcu.cfg
/rom/usr/share/klipper/config/sample-probe-as-z-endstop.cfg
/rom/usr/share/klipper/config/sample-pwm-tool.cfg
/rom/usr/share/klipper/config/sample-raspberry-pi.cfg
/rom/usr/share/klipper/klippy/extras/temperature_sensors.cfg
/rom/usr/share/klipper/test/configs/stm32g431.cfg
/rom/usr/share/klipper/test/configs/stm32h723.cfg
/rom/usr/share/klipper/test/configs/stm32l412.cfg
/rom/usr/share/klipper/test/klippy/bed_screws.cfg
/rom/usr/share/klipper/test/klippy/bltouch.cfg
/rom/usr/share/klipper/test/klippy/delta_calibrate.cfg
/rom/usr/share/klipper/test/klippy/dual_carriage.cfg
/rom/usr/share/klipper/test/klippy/exclude_object.cfg
/rom/usr/share/klipper/test/klippy/extruders.cfg
/rom/usr/share/klipper/test/klippy/gcode_arcs.cfg
/rom/usr/share/klipper/test/klippy/input_shaper.cfg
/rom/usr/share/klipper/test/klippy/led.cfg
/rom/usr/share/klipper/test/klippy/linuxtest.cfg
/rom/usr/share/klipper/test/klippy/macros.cfg
/rom/usr/share/klipper/test/klippy/manual_stepper.cfg
/rom/usr/share/klipper/test/klippy/multi_z.cfg
/rom/usr/share/klipper/test/klippy/pwm.cfg
/rom/usr/share/klipper/test/klippy/rotary_delta_calibrate.cfg
/rom/usr/share/klipper/test/klippy/screws_tilt_adjust.cfg
/rom/usr/share/klipper/test/klippy/sdcard_loop.cfg
/rom/usr/share/klipper/test/klippy/temperature.cfg
/rom/usr/share/klipper/test/klippy/tmc.cfg
/rom/usr/share/klipper/test/klippy/z_tilt.cfg
/rom/usr/share/klipper/test/klippy/z_virtual_endstop.cfg
/rom/usr/share/klippy-env/lib/python3.9/distutils/distutils.cfg
/rom/usr/share/klippy-env/lib/python3.9/site-packages/pip/_vendor/distlib/_backport/sysconfig.cfg
/rom/usr/share/moonraker-env/lib/python3.9/distutils/distutils.cfg
/rom/usr/share/moonraker-env/lib/python3.9/site-packages/pip/_vendor/distlib/_backport/sysconfig.cfg
/usr/lib/python3.9/site-packages/pip/_vendor/distlib/_backport/sysconfig.cfg
/usr/lib/python3.9/site-packages/pycparser/_c_ast.cfg
/usr/lib/python3.9/site-packages/tornado/test/options_test.cfg
/usr/lib/python3.9/site-packages/tornado/test/options_test_types.cfg
/usr/lib/python3.9/site-packages/tornado/test/options_test_types_str.cfg
/usr/share/klipper/config/F008/box.cfg
/usr/share/klipper/config/F008/factory_printer.cfg
/usr/share/klipper/config/F008/gcode_macro.cfg
/usr/share/klipper/config/F008/printer.cfg
/usr/share/klipper/config/F008/printer_params.cfg
/usr/share/klipper/config/F008/sensorless.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/box.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/factory_printer.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/gcode_macro.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/motor_control.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/printer.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/printer_params.cfg
/usr/share/klipper/config/F008_CR0CN240319C13/sensorless.cfg
/usr/share/klipper/config/F008_CR0CN240319C13_1/box.cfg
/usr/share/klipper/config/F008_CR0CN240319C13_1/factory_printer.cfg
/usr/share/klipper/config/F008_CR0CN240319C13_1/gcode_macro.cfg
/usr/share/klipper/config/F008_CR0CN240319C13_1/printer.cfg
/usr/share/klipper/config/F008_CR0CN240319C13_1/printer_params.cfg
/usr/share/klipper/config/F008_CR0CN240319C13_1/sensorless.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/box.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/factory_printer.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/gcode_macro.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/motor_control.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/printer_params.cfg
/usr/share/klipper/config/F012_CR0CN200400C10/sensorless.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/box.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/factory_printer.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/gcode_macro.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/motor_control.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/printer_params.cfg
/usr/share/klipper/config/F021_CR0CN200400C10/sensorless.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/box.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/factory_printer.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/gcode_macro.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/motor_control.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/printer_params.cfg
/usr/share/klipper/config/F025_CR0CN200400C10/sensorless.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/box.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/factory_printer.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/gcode_macro.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/motor_control.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/printer.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/printer_params.cfg
/usr/share/klipper/config/F037_CR5NN251101C10/sensorless.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/box.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/factory_printer.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/gcode_macro.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/motor_control.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/printer.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/printer_params.cfg
/usr/share/klipper/config/F038_CR4SNF038C01/sensorless.cfg
/usr/share/klipper/config/GS_01_CR4CU220812S12/factory_printer.cfg
/usr/share/klipper/config/GS_01_CR4CU220812S12/gcode_macro.cfg
/usr/share/klipper/config/GS_01_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/GS_01_CR4CU220812S12/printer_params.cfg
/usr/share/klipper/config/GS_01_CR4CU220812S12/sensorless.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/box.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/factory_printer.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/gcode_macro.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/motor_control.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/printer.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/printer_params.cfg
/usr/share/klipper/config/GS_03_CR0CN240319C13/sensorless.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/box.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/factory_printer.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/gcode_macro.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/motor_control.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/printer_params.cfg
/usr/share/klipper/config/GS_04_CR0CN200400C10/sensorless.cfg
/usr/share/klipper/config/K1C_CR4CU220812S12/factory_printer.cfg
/usr/share/klipper/config/K1C_CR4CU220812S12/gcode_macro.cfg
/usr/share/klipper/config/K1C_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/K1C_CR4CU220812S12/printer_params.cfg
/usr/share/klipper/config/K1C_CR4CU220812S12/sensorless.cfg
/usr/share/klipper/config/K1_CR4CU220812S10/gcode_macro.cfg
/usr/share/klipper/config/K1_CR4CU220812S10/printer.cfg
/usr/share/klipper/config/K1_CR4CU220812S10/printer_params.cfg
/usr/share/klipper/config/K1_CR4CU220812S10/sensorless.cfg
/usr/share/klipper/config/K1_CR4CU220812S11/gcode_macro.cfg
/usr/share/klipper/config/K1_CR4CU220812S11/printer.cfg
/usr/share/klipper/config/K1_CR4CU220812S11/printer_params.cfg
/usr/share/klipper/config/K1_CR4CU220812S11/sensorless.cfg
/usr/share/klipper/config/K1_CR4CU220812S12/factory_printer.cfg
/usr/share/klipper/config/K1_CR4CU220812S12/gcode_macro.cfg
/usr/share/klipper/config/K1_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/K1_CR4CU220812S12/printer_params.cfg
/usr/share/klipper/config/K1_CR4CU220812S12/sensorless.cfg
/usr/share/klipper/config/K1_MAX_CR0CN240110C10/factory_printer.cfg
/usr/share/klipper/config/K1_MAX_CR0CN240110C10/gcode_macro.cfg
/usr/share/klipper/config/K1_MAX_CR0CN240110C10/printer.cfg
/usr/share/klipper/config/K1_MAX_CR0CN240110C10/printer_params.cfg
/usr/share/klipper/config/K1_MAX_CR0CN240110C10/sensorless.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S11/gcode_macro.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S11/printer.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S11/printer_params.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S11/sensorless.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S12/box.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S12/factory_printer.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S12/gcode_macro.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S12/printer_params.cfg
/usr/share/klipper/config/K1_MAX_CR4CU220812S12/sensorless.cfg
/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/factory_printer.cfg
/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/gcode_macro.cfg
/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/printer.cfg
/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/printer_params.cfg
/usr/share/klipper/config/K1_MAX_SE_CR4CU220812S12/sensorless.cfg
/usr/share/klipper/config/PF027_CR0CN250701C10/box.cfg
/usr/share/klipper/config/PF027_CR0CN250701C10/factory_printer.cfg
/usr/share/klipper/config/PF027_CR0CN250701C10/gcode_macro.cfg
/usr/share/klipper/config/PF027_CR0CN250701C10/printer.cfg
/usr/share/klipper/config/PF027_CR0CN250701C10/printer_params.cfg
/usr/share/klipper/config/PF027_CR0CN250701C10/sensorless.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/box.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/factory_printer.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/gcode_macro.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/motor_control.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/printer.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/printer_params.cfg
/usr/share/klipper/config/Z2_CR0CN200400C10/sensorless.cfg
/usr/share/klipper/config/example-cartesian.cfg
/usr/share/klipper/config/example-corexy.cfg
/usr/share/klipper/config/example-corexz.cfg
/usr/share/klipper/config/example-delta.cfg
/usr/share/klipper/config/example-deltesian.cfg
/usr/share/klipper/config/example-extras.cfg
/usr/share/klipper/config/example-hybrid-corexy.cfg
/usr/share/klipper/config/example-hybrid-corexz.cfg
/usr/share/klipper/config/example-polar.cfg
/usr/share/klipper/config/example-rotary-delta.cfg
/usr/share/klipper/config/example-winch.cfg
/usr/share/klipper/config/example.cfg
/usr/share/klipper/config/generic-alligator-r2.cfg
/usr/share/klipper/config/generic-alligator-r3.cfg
/usr/share/klipper/config/generic-archim2.cfg
/usr/share/klipper/config/generic-azteeg-x5-mini-v3.cfg
/usr/share/klipper/config/generic-bigtreetech-e3-rrf-v1.1.cfg
/usr/share/klipper/config/generic-bigtreetech-gtr.cfg
/usr/share/klipper/config/generic-bigtreetech-manta-m4p.cfg
/usr/share/klipper/config/generic-bigtreetech-manta-m8p.cfg
/usr/share/klipper/config/generic-bigtreetech-octopus.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-2.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-3.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-cr6-v1.0.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-e3-dip.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-e3-turbo.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v1.0.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v1.2.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v2.0.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-mini-e3-v3.0.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-mini-mz.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-mini.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-pico-v1.0.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-pro.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-v1.1.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-v1.3.cfg
/usr/share/klipper/config/generic-bigtreetech-skr-v1.4.cfg
/usr/share/klipper/config/generic-cramps.cfg
/usr/share/klipper/config/generic-creality-v4.2.10.cfg
/usr/share/klipper/config/generic-creality-v4.2.7.cfg
/usr/share/klipper/config/generic-duet2-duex.cfg
/usr/share/klipper/config/generic-duet2-maestro.cfg
/usr/share/klipper/config/generic-duet2.cfg
/usr/share/klipper/config/generic-duet3-mini.cfg
/usr/share/klipper/config/generic-einsy-rambo.cfg
/usr/share/klipper/config/generic-flyboard.cfg
/usr/share/klipper/config/generic-fysetc-cheetah-v1.1.cfg
/usr/share/klipper/config/generic-fysetc-cheetah-v1.2.cfg
/usr/share/klipper/config/generic-fysetc-f6.cfg
/usr/share/klipper/config/generic-fysetc-s6-v2.cfg
/usr/share/klipper/config/generic-fysetc-s6.cfg
/usr/share/klipper/config/generic-fysetc-spider.cfg
/usr/share/klipper/config/generic-gt2560.cfg
/usr/share/klipper/config/generic-mellow-fly-cdy-v3.cfg
/usr/share/klipper/config/generic-mellow-fly-gemini-v1.cfg
/usr/share/klipper/config/generic-mellow-fly-gemini-v2.cfg
/usr/share/klipper/config/generic-mellow-super-infinty-hv.cfg
/usr/share/klipper/config/generic-melzi.cfg
/usr/share/klipper/config/generic-mightyboard.cfg
/usr/share/klipper/config/generic-mini-rambo.cfg
/usr/share/klipper/config/generic-minitronics1.cfg
/usr/share/klipper/config/generic-mks-robin-e3.cfg
/usr/share/klipper/config/generic-mks-robin-nano-v1.cfg
/usr/share/klipper/config/generic-mks-robin-nano-v2.cfg
/usr/share/klipper/config/generic-mks-robin-nano-v3.cfg
/usr/share/klipper/config/generic-mks-rumba32-v1.0.cfg
/usr/share/klipper/config/generic-mks-sgenl.cfg
/usr/share/klipper/config/generic-printrboard-g2.cfg
/usr/share/klipper/config/generic-printrboard.cfg
/usr/share/klipper/config/generic-prusa-buddy.cfg
/usr/share/klipper/config/generic-radds.cfg
/usr/share/klipper/config/generic-rambo.cfg
/usr/share/klipper/config/generic-ramps.cfg
/usr/share/klipper/config/generic-re-arm.cfg
/usr/share/klipper/config/generic-replicape.cfg
/usr/share/klipper/config/generic-rumba.cfg
/usr/share/klipper/config/generic-ruramps-v1.3.cfg
/usr/share/klipper/config/generic-simulavr.cfg
/usr/share/klipper/config/generic-smoothieboard.cfg
/usr/share/klipper/config/generic-th3d-ezboard-lite-v1.2.cfg
/usr/share/klipper/config/generic-th3d-ezboard-lite-v2.0.cfg
/usr/share/klipper/config/generic-ultimaker-ultimainboard-v2.cfg
/usr/share/klipper/config/kit-voron2-250mm.cfg
/usr/share/klipper/config/kit-zav3d-2019.cfg
/usr/share/klipper/config/printer-adimlab-2018.cfg
/usr/share/klipper/config/printer-alfawise-u30-2018.cfg
/usr/share/klipper/config/printer-anet-a4-2018.cfg
/usr/share/klipper/config/printer-anet-a8-2017.cfg
/usr/share/klipper/config/printer-anet-a8-2019.cfg
/usr/share/klipper/config/printer-anet-e10-2018.cfg
/usr/share/klipper/config/printer-anet-e16-2019.cfg
/usr/share/klipper/config/printer-anycubic-4max-2018.cfg
/usr/share/klipper/config/printer-anycubic-4maxpro-2.0-2021.cfg
/usr/share/klipper/config/printer-anycubic-i3-mega-2017.cfg
/usr/share/klipper/config/printer-anycubic-kossel-2016.cfg
/usr/share/klipper/config/printer-anycubic-kossel-plus-2017.cfg
/usr/share/klipper/config/printer-anycubic-vyper-2021.cfg
/usr/share/klipper/config/printer-artillery-sidewinder-x2-2022.cfg
/usr/share/klipper/config/printer-biqu-b1-se-plus-2022.cfg
/usr/share/klipper/config/printer-biqu-bx-2021.cfg
/usr/share/klipper/config/printer-bq-hephestos-2014.cfg
/usr/share/klipper/config/printer-creality-cr10-2017.cfg
/usr/share/klipper/config/printer-creality-cr10-smart-pro-2022.cfg
/usr/share/klipper/config/printer-creality-cr10-v3-2020.cfg
/usr/share/klipper/config/printer-creality-cr10mini-2017.cfg
/usr/share/klipper/config/printer-creality-cr10s-2017.cfg
/usr/share/klipper/config/printer-creality-cr20-2018.cfg
/usr/share/klipper/config/printer-creality-cr20-pro-2019.cfg
/usr/share/klipper/config/printer-creality-cr30-2021.cfg
/usr/share/klipper/config/printer-creality-cr6se-2020.cfg
/usr/share/klipper/config/printer-creality-cr6se-2021.cfg
/usr/share/klipper/config/printer-creality-ender2-2017.cfg
/usr/share/klipper/config/printer-creality-ender2pro-2021.cfg
/usr/share/klipper/config/printer-creality-ender3-2018.cfg
/usr/share/klipper/config/printer-creality-ender3-s1-2021.cfg
/usr/share/klipper/config/printer-creality-ender3-s1plus-2022.cfg
/usr/share/klipper/config/printer-creality-ender3-v2-2020.cfg
/usr/share/klipper/config/printer-creality-ender3max-2021.cfg
/usr/share/klipper/config/printer-creality-ender3pro-2020.cfg
/usr/share/klipper/config/printer-creality-ender5-2019.cfg
/usr/share/klipper/config/printer-creality-ender5plus-2019.cfg
/usr/share/klipper/config/printer-creality-ender5pro-2020.cfg
/usr/share/klipper/config/printer-creality-ender6-2020.cfg
/usr/share/klipper/config/printer-creality-sermoonD1-2021.cfg
/usr/share/klipper/config/printer-creality-sermoonV1-2022.cfg
/usr/share/klipper/config/printer-elegoo-neptune2-2021.cfg
/usr/share/klipper/config/printer-eryone-er20-2021.cfg
/usr/share/klipper/config/printer-eryone-thinker-series-v2-2020.cfg
/usr/share/klipper/config/printer-flashforge-creator-pro-2018.cfg
/usr/share/klipper/config/printer-flsun-q5-2020.cfg
/usr/share/klipper/config/printer-flsun-qqs-2020.cfg
/usr/share/klipper/config/printer-fokoos-odin5-f3-2021.cfg
/usr/share/klipper/config/printer-geeetech-301-2019.cfg
/usr/share/klipper/config/printer-hiprecy-leo-2019.cfg
/usr/share/klipper/config/printer-longer-lk4-pro-2019.cfg
/usr/share/klipper/config/printer-lulzbot-mini1-2016.cfg
/usr/share/klipper/config/printer-lulzbot-taz6-2017.cfg
/usr/share/klipper/config/printer-lulzbot-taz6-dual-v3-2017.cfg
/usr/share/klipper/config/printer-makergear-m2-2012.cfg
/usr/share/klipper/config/printer-makergear-m2-2016.cfg
/usr/share/klipper/config/printer-micromake-d1-2016.cfg
/usr/share/klipper/config/printer-modix-big60-2020.cfg
/usr/share/klipper/config/printer-monoprice-mini-delta-2017.cfg
/usr/share/klipper/config/printer-monoprice-select-mini-v1-2016.cfg
/usr/share/klipper/config/printer-monoprice-select-mini-v2-2018.cfg
/usr/share/klipper/config/printer-mtw-create-2015.cfg
/usr/share/klipper/config/printer-prusa-mini-plus-2020.cfg
/usr/share/klipper/config/printer-robo3d-r2-2017.cfg
/usr/share/klipper/config/printer-seemecnc-rostock-max-v2-2015.cfg
/usr/share/klipper/config/printer-sovol-sv01-2020.cfg
/usr/share/klipper/config/printer-sunlu-s8-2020.cfg
/usr/share/klipper/config/printer-tevo-flash-2018.cfg
/usr/share/klipper/config/printer-tevo-tarantula-pro-2020.cfg
/usr/share/klipper/config/printer-tronxy-p802e-2020.cfg
/usr/share/klipper/config/printer-tronxy-p802m-2020.cfg
/usr/share/klipper/config/printer-tronxy-x5s-2018.cfg
/usr/share/klipper/config/printer-tronxy-x5sa-pro-2020.cfg
/usr/share/klipper/config/printer-tronxy-x5sa-v6-2019.cfg
/usr/share/klipper/config/printer-tronxy-x8-2018.cfg
/usr/share/klipper/config/printer-tronxy-xy-2-Pro-2020.cfg
/usr/share/klipper/config/printer-twotrees-sapphire-plus-sp-5-v1-2020.cfg
/usr/share/klipper/config/printer-twotrees-sapphire-plus-sp-5-v1.1-2021.cfg
/usr/share/klipper/config/printer-twotrees-sapphire-pro-sp-3-2020.cfg
/usr/share/klipper/config/printer-velleman-k8200-2013.cfg
/usr/share/klipper/config/printer-velleman-k8800-2017.cfg
/usr/share/klipper/config/printer-wanhao-duplicator-6-2016.cfg
/usr/share/klipper/config/printer-wanhao-duplicator-9-2018.cfg
/usr/share/klipper/config/printer-wanhao-duplicator-i3-mini-2017.cfg
/usr/share/klipper/config/printer-wanhao-duplicator-i3-plus-2017.cfg
/usr/share/klipper/config/printer-wanhao-duplicator-i3-plus-mark2-2019.cfg
/usr/share/klipper/config/printer-wanhao-duplicator-i3-v2.1-2017.cfg
/usr/share/klipper/config/sample-aliases.cfg
/usr/share/klipper/config/sample-bigtreetech-ebb-canbus-v1.0.cfg
/usr/share/klipper/config/sample-bigtreetech-ebb-canbus-v1.1.cfg
/usr/share/klipper/config/sample-bigtreetech-exp-mot.cfg
/usr/share/klipper/config/sample-bigtreetech-hermit-crab-canbus.cfg
/usr/share/klipper/config/sample-glyphs.cfg
/usr/share/klipper/config/sample-huvud-v0.61.cfg
/usr/share/klipper/config/sample-idex.cfg
/usr/share/klipper/config/sample-lcd.cfg
/usr/share/klipper/config/sample-macros.cfg
/usr/share/klipper/config/sample-mmu2s-diy.cfg
/usr/share/klipper/config/sample-multi-extruder.cfg
/usr/share/klipper/config/sample-multi-mcu.cfg
/usr/share/klipper/config/sample-probe-as-z-endstop.cfg
/usr/share/klipper/config/sample-pwm-tool.cfg
/usr/share/klipper/config/sample-raspberry-pi.cfg
/usr/share/klipper/klippy/extras/temperature_sensors.cfg
/usr/share/klipper/test/configs/stm32g431.cfg
/usr/share/klipper/test/configs/stm32h723.cfg
/usr/share/klipper/test/configs/stm32l412.cfg
/usr/share/klipper/test/klippy/bed_screws.cfg
/usr/share/klipper/test/klippy/bltouch.cfg
/usr/share/klipper/test/klippy/delta_calibrate.cfg
/usr/share/klipper/test/klippy/dual_carriage.cfg
/usr/share/klipper/test/klippy/exclude_object.cfg
/usr/share/klipper/test/klippy/extruders.cfg
/usr/share/klipper/test/klippy/gcode_arcs.cfg
/usr/share/klipper/test/klippy/input_shaper.cfg
/usr/share/klipper/test/klippy/led.cfg
/usr/share/klipper/test/klippy/linuxtest.cfg
/usr/share/klipper/test/klippy/macros.cfg
/usr/share/klipper/test/klippy/manual_stepper.cfg
/usr/share/klipper/test/klippy/multi_z.cfg
/usr/share/klipper/test/klippy/pwm.cfg
/usr/share/klipper/test/klippy/rotary_delta_calibrate.cfg
/usr/share/klipper/test/klippy/screws_tilt_adjust.cfg
/usr/share/klipper/test/klippy/sdcard_loop.cfg
/usr/share/klipper/test/klippy/temperature.cfg
/usr/share/klipper/test/klippy/tmc.cfg
/usr/share/klipper/test/klippy/z_tilt.cfg
/usr/share/klipper/test/klippy/z_virtual_endstop.cfg
/usr/share/klippy-env/lib/python3.9/distutils/distutils.cfg
/usr/share/klippy-env/lib/python3.9/site-packages/pip/_vendor/distlib/_backport/sysconfig.cfg
/usr/share/moonraker-env/lib/python3.9/distutils/distutils.cfg
/usr/share/moonraker-env/lib/python3.9/site-packages/pip/_vendor/distlib/_backport/sysconfig.cfg


root@K2Plus-DBD5:~# find / -name "*.conf" 2>/dev/null
/etc/asound.conf
/etc/cedarc.conf
/etc/cedarx.conf
/etc/e2fsck.conf
/etc/nginx/nginx.conf
/etc/nginx/uci.conf
/etc/opkg/distfeeds.conf
/etc/pip.conf
/etc/resolv.conf
/etc/sysctl.conf
/etc/sysctl.d/10-default.conf
/etc/sysupgrade.conf
/etc/udev/udev.conf
/etc/wifi/hostapd/hostapd.conf
/etc/wifi/wifi_monitor.conf
/etc/wifi/wpa_supplicant/wpa_supplicant.conf
/etc/wifi/wpa_supplicant/wpa_supplicant_overlay.conf
/etc/wifi/wpa_supplicant/wpa_supplicant_p2p.conf
/etc/wifi/wpa_supplicant/wpa_supplicant_src.conf
/etc/xattr.conf
/overlay/upper/usr/share/moonraker/moonraker.conf
/overlay/upper/usr/share/moonraker_backup/moonraker.conf
/overlay/upper/etc/wifi/wpa_supplicant/wpa_supplicant.conf
/overlay/upper/root/K2-Camera-main/moonraker/moonraker.conf
/rom/etc/asound.conf
/rom/etc/cedarc.conf
/rom/etc/cedarx.conf
/rom/etc/e2fsck.conf
/rom/etc/nginx/nginx.conf
/rom/etc/nginx/uci.conf
/rom/etc/opkg/distfeeds.conf
/rom/etc/pip.conf
/rom/etc/resolv.conf
/rom/etc/sysctl.conf
/rom/etc/sysctl.d/10-default.conf
/rom/etc/sysupgrade.conf
/rom/etc/udev/udev.conf
/rom/etc/wifi/hostapd/hostapd.conf
/rom/etc/wifi/wifi_monitor.conf
/rom/etc/wifi/wpa_supplicant/wpa_supplicant.conf
/rom/etc/wifi/wpa_supplicant/wpa_supplicant_overlay.conf
/rom/etc/wifi/wpa_supplicant/wpa_supplicant_p2p.conf
/rom/etc/wifi/wpa_supplicant/wpa_supplicant_src.conf
/rom/etc/xattr.conf
/rom/usr/share/alsa/alsa.conf
/rom/usr/share/alsa/cards/AACI.conf
/rom/usr/share/alsa/cards/ATIIXP-MODEM.conf
/rom/usr/share/alsa/cards/ATIIXP-SPDMA.conf
/rom/usr/share/alsa/cards/ATIIXP.conf
/rom/usr/share/alsa/cards/AU8810.conf
/rom/usr/share/alsa/cards/AU8820.conf
/rom/usr/share/alsa/cards/AU8830.conf
/rom/usr/share/alsa/cards/Audigy.conf
/rom/usr/share/alsa/cards/Audigy2.conf
/rom/usr/share/alsa/cards/Aureon51.conf
/rom/usr/share/alsa/cards/Aureon71.conf
/rom/usr/share/alsa/cards/CA0106.conf
/rom/usr/share/alsa/cards/CMI8338-SWIEC.conf
/rom/usr/share/alsa/cards/CMI8338.conf
/rom/usr/share/alsa/cards/CMI8738-MC6.conf
/rom/usr/share/alsa/cards/CMI8738-MC8.conf
/rom/usr/share/alsa/cards/CMI8788.conf
/rom/usr/share/alsa/cards/CS46xx.conf
/rom/usr/share/alsa/cards/EMU10K1.conf
/rom/usr/share/alsa/cards/EMU10K1X.conf
/rom/usr/share/alsa/cards/ENS1370.conf
/rom/usr/share/alsa/cards/ENS1371.conf
/rom/usr/share/alsa/cards/ES1968.conf
/rom/usr/share/alsa/cards/Echo_Echo3G.conf
/rom/usr/share/alsa/cards/FM801.conf
/rom/usr/share/alsa/cards/FWSpeakers.conf
/rom/usr/share/alsa/cards/FireWave.conf
/rom/usr/share/alsa/cards/GUS.conf
/rom/usr/share/alsa/cards/HDA-Intel.conf
/rom/usr/share/alsa/cards/HdmiLpeAudio.conf
/rom/usr/share/alsa/cards/ICE1712.conf
/rom/usr/share/alsa/cards/ICE1724.conf
/rom/usr/share/alsa/cards/ICH-MODEM.conf
/rom/usr/share/alsa/cards/ICH.conf
/rom/usr/share/alsa/cards/ICH4.conf
/rom/usr/share/alsa/cards/Loopback.conf
/rom/usr/share/alsa/cards/Maestro3.conf
/rom/usr/share/alsa/cards/NFORCE.conf
/rom/usr/share/alsa/cards/PC-Speaker.conf
/rom/usr/share/alsa/cards/PMac.conf
/rom/usr/share/alsa/cards/PMacToonie.conf
/rom/usr/share/alsa/cards/PS3.conf
/rom/usr/share/alsa/cards/RME9636.conf
/rom/usr/share/alsa/cards/RME9652.conf
/rom/usr/share/alsa/cards/SB-XFi.conf
/rom/usr/share/alsa/cards/SI7018.conf
/rom/usr/share/alsa/cards/TRID4DWAVENX.conf
/rom/usr/share/alsa/cards/USB-Audio.conf
/rom/usr/share/alsa/cards/VIA686A.conf
/rom/usr/share/alsa/cards/VIA8233.conf
/rom/usr/share/alsa/cards/VIA8233A.conf
/rom/usr/share/alsa/cards/VIA8237.conf
/rom/usr/share/alsa/cards/VX222.conf
/rom/usr/share/alsa/cards/VXPocket.conf
/rom/usr/share/alsa/cards/VXPocket440.conf
/rom/usr/share/alsa/cards/YMF744.conf
/rom/usr/share/alsa/cards/aliases.conf
/rom/usr/share/alsa/cards/pistachio-card.conf
/rom/usr/share/alsa/cards/vc4-hdmi.conf
/rom/usr/share/alsa/pcm/center_lfe.conf
/rom/usr/share/alsa/pcm/default.conf
/rom/usr/share/alsa/pcm/dmix.conf
/rom/usr/share/alsa/pcm/dpl.conf
/rom/usr/share/alsa/pcm/dsnoop.conf
/rom/usr/share/alsa/pcm/front.conf
/rom/usr/share/alsa/pcm/hdmi.conf
/rom/usr/share/alsa/pcm/iec958.conf
/rom/usr/share/alsa/pcm/modem.conf
/rom/usr/share/alsa/pcm/rear.conf
/rom/usr/share/alsa/pcm/side.conf
/rom/usr/share/alsa/pcm/surround21.conf
/rom/usr/share/alsa/pcm/surround40.conf
/rom/usr/share/alsa/pcm/surround41.conf
/rom/usr/share/alsa/pcm/surround50.conf
/rom/usr/share/alsa/pcm/surround51.conf
/rom/usr/share/alsa/pcm/surround71.conf
/rom/usr/share/dbus-1/session.conf
/rom/usr/share/dbus-1/system.conf
/rom/usr/share/moonraker/moonraker.conf
/root/K2-Camera-main/moonraker/moonraker.conf
/tmp/resolv.conf
/usr/share/alsa/alsa.conf
/usr/share/alsa/cards/AACI.conf
/usr/share/alsa/cards/ATIIXP-MODEM.conf
/usr/share/alsa/cards/ATIIXP-SPDMA.conf
/usr/share/alsa/cards/ATIIXP.conf
/usr/share/alsa/cards/AU8810.conf
/usr/share/alsa/cards/AU8820.conf
/usr/share/alsa/cards/AU8830.conf
/usr/share/alsa/cards/Audigy.conf
/usr/share/alsa/cards/Audigy2.conf
/usr/share/alsa/cards/Aureon51.conf
/usr/share/alsa/cards/Aureon71.conf
/usr/share/alsa/cards/CA0106.conf
/usr/share/alsa/cards/CMI8338-SWIEC.conf
/usr/share/alsa/cards/CMI8338.conf
/usr/share/alsa/cards/CMI8738-MC6.conf
/usr/share/alsa/cards/CMI8738-MC8.conf
/usr/share/alsa/cards/CMI8788.conf
/usr/share/alsa/cards/CS46xx.conf
/usr/share/alsa/cards/EMU10K1.conf
/usr/share/alsa/cards/EMU10K1X.conf
/usr/share/alsa/cards/ENS1370.conf
/usr/share/alsa/cards/ENS1371.conf
/usr/share/alsa/cards/ES1968.conf
/usr/share/alsa/cards/Echo_Echo3G.conf
/usr/share/alsa/cards/FM801.conf
/usr/share/alsa/cards/FWSpeakers.conf
/usr/share/alsa/cards/FireWave.conf
/usr/share/alsa/cards/GUS.conf
/usr/share/alsa/cards/HDA-Intel.conf
/usr/share/alsa/cards/HdmiLpeAudio.conf
/usr/share/alsa/cards/ICE1712.conf
/usr/share/alsa/cards/ICE1724.conf
/usr/share/alsa/cards/ICH-MODEM.conf
/usr/share/alsa/cards/ICH.conf
/usr/share/alsa/cards/ICH4.conf
/usr/share/alsa/cards/Loopback.conf
/usr/share/alsa/cards/Maestro3.conf
/usr/share/alsa/cards/NFORCE.conf
/usr/share/alsa/cards/PC-Speaker.conf
/usr/share/alsa/cards/PMac.conf
/usr/share/alsa/cards/PMacToonie.conf
/usr/share/alsa/cards/PS3.conf
/usr/share/alsa/cards/RME9636.conf
/usr/share/alsa/cards/RME9652.conf
/usr/share/alsa/cards/SB-XFi.conf
/usr/share/alsa/cards/SI7018.conf
/usr/share/alsa/cards/TRID4DWAVENX.conf
/usr/share/alsa/cards/USB-Audio.conf
/usr/share/alsa/cards/VIA686A.conf
/usr/share/alsa/cards/VIA8233.conf
/usr/share/alsa/cards/VIA8233A.conf
/usr/share/alsa/cards/VIA8237.conf
/usr/share/alsa/cards/VX222.conf
/usr/share/alsa/cards/VXPocket.conf
/usr/share/alsa/cards/VXPocket440.conf
/usr/share/alsa/cards/YMF744.conf
/usr/share/alsa/cards/aliases.conf
/usr/share/alsa/cards/pistachio-card.conf
/usr/share/alsa/cards/vc4-hdmi.conf
/usr/share/alsa/pcm/center_lfe.conf
/usr/share/alsa/pcm/default.conf
/usr/share/alsa/pcm/dmix.conf
/usr/share/alsa/pcm/dpl.conf
/usr/share/alsa/pcm/dsnoop.conf
/usr/share/alsa/pcm/front.conf
/usr/share/alsa/pcm/hdmi.conf
/usr/share/alsa/pcm/iec958.conf
/usr/share/alsa/pcm/modem.conf
/usr/share/alsa/pcm/rear.conf
/usr/share/alsa/pcm/side.conf
/usr/share/alsa/pcm/surround21.conf
/usr/share/alsa/pcm/surround40.conf
/usr/share/alsa/pcm/surround41.conf
/usr/share/alsa/pcm/surround50.conf
/usr/share/alsa/pcm/surround51.conf
/usr/share/alsa/pcm/surround71.conf
/usr/share/dbus-1/session.conf
/usr/share/dbus-1/system.conf
/usr/share/moonraker/moonraker.conf
/usr/share/moonraker_backup/moonraker.conf


root@K2Plus-DBD5:~# find / -name "*.gcode" 2>/dev/null
/etc/sysConfig/defData/Auto_Em.gcode
/etc/sysConfig/defData/Auto_pressure_advance_multi.gcode
/etc/sysConfig/defData/Auto_pressure_advance_testpadvance.gcode
/etc/sysConfig/defData/Auto_pressure_advance_testpadvance_product_test.gcode
/etc/sysConfig/defData/auto_laser_test.gcode
/etc/sysConfig/defData/laser_offset_correction.gcode
/etc/sysConfig/defData/laser_offset_correction_0.2mm.gcode
/etc/sysConfig/defData/laser_test_line.gcode
/etc/sysConfig/defData/line_width_height.gcode
/mnt/UDISK/printer_data/gcodes/Valve Knob v2.stl_PLA_7m53s.gcode
/mnt/UDISK/printer_data/gcodes/race_way.stl_PLA_2h21m32s.gcode
/mnt/UDISK/printer_data/gcodes/Body7.stl_PLA_42m0s.gcode
/mnt/UDISK/printer_data/gcodes/Component10.stl_1_PLA_2h24m15s.gcode
/mnt/UDISK/printer_data/gcodes/Clitoris v8.stl_PLA_8m8s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_32m50s.gcode
/mnt/UDISK/printer_data/gcodes/Lid.stl_PETG_46m12s.gcode
/mnt/UDISK/printer_data/gcodes/Bearing Spindle Part1.stl_PLA_2h56m58s.gcode
/mnt/UDISK/printer_data/gcodes/Cover Plate.stl_PLA_26m29s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h1m56s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_21m5s.gcode
/mnt/UDISK/printer_data/gcodes/Clitoris v8.stl_PLA_33m27s.gcode
/mnt/UDISK/printer_data/gcodes/CPAP_Hose_Coupler.stl_PETG_2h1m5s.gcode
/mnt/UDISK/printer_data/gcodes/Cube_PLA_19m30s.gcode
/mnt/UDISK/printer_data/gcodes/Clitoris v8.stl_PLA_26m59s.gcode
/mnt/UDISK/printer_data/gcodes/Case.stl_PLA_1h30m52s.gcode
/mnt/UDISK/printer_data/gcodes/WeaveBobbin v2.stl_PLA_4m20s.gcode
/mnt/UDISK/printer_data/gcodes/Component10.stl_1_PLA_2h53m51s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_22m46s.gcode
/mnt/UDISK/printer_data/gcodes/PcbPlateDummy v2.stl_PLA_55m24s.gcode
/mnt/UDISK/printer_data/gcodes/LidLong.stl_PETG_55m36s.gcode
/mnt/UDISK/printer_data/gcodes/Body6.stl_PLA_17m47s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_11m23s.gcode
/mnt/UDISK/printer_data/gcodes/9e8b5823-52b9-4892-ba8c-a2dfc7289e96.stl_PLA_57m35s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_13m2s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_9m53s.gcode
/mnt/UDISK/printer_data/gcodes/Crealitylogo_PLA_32m41s.gcode
/mnt/UDISK/printer_data/gcodes/Boardcliptest v2.stl_PLA_7m10s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_1h55m13s.gcode
/mnt/UDISK/printer_data/gcodes/Component2.stl_PLA_37m23s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_24m1s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_25m22s.gcode
/mnt/UDISK/printer_data/gcodes/Hexa Axle 128mm.stl_PLA_17m7s.gcode
/mnt/UDISK/printer_data/gcodes/AngledCogs v1.stl_1_PLA_36m43s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h29m26s.gcode
/mnt/UDISK/printer_data/gcodes/YarnSwift v17.stl_1_PLA_6h50m43s.gcode
/mnt/UDISK/printer_data/gcodes/GiftBoxTemplate v5.stl_PLA_3h2m2s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_2h7m7s.gcode
/mnt/UDISK/printer_data/gcodes/Component3.stl_PLA_25m34s.gcode
/mnt/UDISK/printer_data/gcodes/LattePandaScreenCase v2.stl_PLA_40m47s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_6h41m19s.gcode
/mnt/UDISK/printer_data/gcodes/Oculus+Meta+Quest+2+and+Quest+3+Mount.stl_PETG_1h52m59s.gcode
/mnt/UDISK/printer_data/gcodes/Mustang Tire_PLA_5m12s.gcode
/mnt/UDISK/printer_data/gcodes/RailClipCap.stl_PETG_18m0s.gcode
/mnt/UDISK/printer_data/gcodes/Ipad stand.stl_PLA_40m59s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_53m52s.gcode
/mnt/UDISK/printer_data/gcodes/filament_guide_carriage+slides&Bearing.stl_PLA_5h10m35s.gcode
/mnt/UDISK/printer_data/gcodes/Whiteboard Brackets.stl_PLA_2m22s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_2m59s.gcode
/mnt/UDISK/printer_data/gcodes/BoilerShield v8.stl_PETG_15h42m7s.gcode
/mnt/UDISK/printer_data/gcodes/Pin.stl_1_PLA_45m42s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h47m6s.gcode
/mnt/UDISK/printer_data/gcodes/Component2.stl_PLA_38m4s.gcode
/mnt/UDISK/printer_data/gcodes/spinny_dervish_asm v1.stl_7_PLA_8h16m27s.gcode
/mnt/UDISK/printer_data/gcodes/yarnholder v1.stl_1_PLA_2h49m39s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_2h36m26s.gcode
/mnt/UDISK/printer_data/gcodes/Box.stl_PLA_38m36s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_13m18s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_3h44m1s.gcode
/mnt/UDISK/printer_data/gcodes/K2 Plus - Chute Retainer.stl_PLA_15m28s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h46m44s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4_ABS_1h10m.gcode
/mnt/UDISK/printer_data/gcodes/spacer.stl_PLA_20m39s.gcode
/mnt/UDISK/printer_data/gcodes/BoilerShield v8.stl_PETG_15h43m2s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_15m2s.gcode
/mnt/UDISK/printer_data/gcodes/ScrewdriverBits v3.stl_PLA_28m23s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_11m54s.gcode
/mnt/UDISK/printer_data/gcodes/ROD.stl_PLA_1h7m54s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_12m11s.gcode
/mnt/UDISK/printer_data/gcodes/Component9.stl_PLA_32m45s.gcode
/mnt/UDISK/printer_data/gcodes/50teeth gear.stl_PLA_29m32s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_3h18m27s.gcode
/mnt/UDISK/printer_data/gcodes/Body6.stl_PLA_17m13s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h2m8s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_12m23s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_14m59s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_36m39s.gcode
/mnt/UDISK/printer_data/gcodes/race_way.stl_PLA_1h24m39s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PETG_22m25s.gcode
/mnt/UDISK/printer_data/gcodes/BallWinderCap v5.stl_PLA_9m57s.gcode
/mnt/UDISK/printer_data/gcodes/retainer_clip.stl_PLA_4m26s.gcode
/mnt/UDISK/printer_data/gcodes/DeskTidy.stl_PETG_2h21m36s.gcode
/mnt/UDISK/printer_data/gcodes/ScrewdriverBits v3.stl_TPU_1h55m7s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_3h6m28s.gcode
/mnt/UDISK/printer_data/gcodes/Body5.stl_PLA_23m19s.gcode
/mnt/UDISK/printer_data/gcodes/DuctFanAdaptor v3_PLA_1h28m.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_1h52m30s.gcode
/mnt/UDISK/printer_data/gcodes/Parametric Hinged Box_250 mm box_Lid Assmebly.stl_1_PETG_1h38m59s.gcode
/mnt/UDISK/printer_data/gcodes/part185110_part187439_shrine-s320210105-30702-1bitsk5.stl_ABS_1h8m13s.gcode
/mnt/UDISK/printer_data/gcodes/M8x80BoltAndNut v1.stl_PLA_24m8s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_8h36m16s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_ABS_7h12m7s.gcode
/mnt/UDISK/printer_data/gcodes/M8x80BoltAndNut v1.stl_1_PLA_2m38s.gcode
/mnt/UDISK/printer_data/gcodes/WhiteboardBracketHanger.stl_PLA_51m40s.gcode
/mnt/UDISK/printer_data/gcodes/Yarn Bowl.stl_PLA_3h21m29s.gcode
/mnt/UDISK/printer_data/gcodes/Cronos_Panel.obj_PLA_52m43s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_4h24m56s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_52m10s.gcode
/mnt/UDISK/printer_data/gcodes/Parametric Hinged Box_250 mm box_Lid Assmebly.stl_1_PETG_1h46m54s.gcode
/mnt/UDISK/printer_data/gcodes/3dPrintedgiftBox v2.stl_PLA_13m2s.gcode
/mnt/UDISK/printer_data/gcodes/3dPrintedgiftBox v2.stl_PLA_13m19s.gcode
/mnt/UDISK/printer_data/gcodes/Quest_Wall_Mount_V3.85.STL_PETG_3h36m43s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h39m23s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h15m41s.gcode
/mnt/UDISK/printer_data/gcodes/Oculus+Meta+Quest+2+and+Quest+3+Mount.stl_PLA_1h36m27s.gcode
/mnt/UDISK/printer_data/gcodes/WeavweBobbin3 v4.stl_PLA_10m54s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h16m51s.gcode
/mnt/UDISK/printer_data/gcodes/Ball Nut.stl_8_PLA_12m59s.gcode
/mnt/UDISK/printer_data/gcodes/Component2.stl_PLA_27m16s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_5m36s.gcode
/mnt/UDISK/printer_data/gcodes/Body1_PETG_33m12s.gcode
/mnt/UDISK/printer_data/gcodes/Case.stl_PLA_1h23m56s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_26m12s.gcode
/mnt/UDISK/printer_data/gcodes/Name_Plate.stl_PLA_5h53m2s.gcode
/mnt/UDISK/printer_data/gcodes/Clear Cover.stl_PLA_1h30m38s.gcode
/mnt/UDISK/printer_data/gcodes/PCBPlate.stl_PLA_10m43s.gcode
/mnt/UDISK/printer_data/gcodes/Body11.stl_PLA_1h11m7s.gcode
/mnt/UDISK/printer_data/gcodes/Body7.stl_PLA_20m55s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h7m30s.gcode
/mnt/UDISK/printer_data/gcodes/Body4.stl_PLA_8m7s.gcode
/mnt/UDISK/printer_data/gcodes/3DBenchy.stl_PLA_31m8s.gcode
/mnt/UDISK/printer_data/gcodes/LaserCutterFanAdaptor v3.stl_PLA_56m34s.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v4.stl_PLA_10m27s.gcode
/mnt/UDISK/printer_data/gcodes/Spoolwinder adapter.stl_PLA_26m35s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_2h28m54s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_23h4m19s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_29m30s.gcode
/mnt/UDISK/printer_data/gcodes/Body11.stl_PLA_1h47m26s.gcode
/mnt/UDISK/printer_data/gcodes/WD2 Bouchon.STL_PLA_17m29s.gcode
/mnt/UDISK/printer_data/gcodes/Body4.stl_PLA_30m31s.gcode
/mnt/UDISK/printer_data/gcodes/Mustang Tire.stl_TPU_6m50s.gcode
/mnt/UDISK/printer_data/gcodes/ROD.stl_PLA_1h8m17s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_TPU_3h23m19s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h31m16s.gcode
/mnt/UDISK/printer_data/gcodes/Cronos_Base.obj_PLA_3h2m2s.gcode
/mnt/UDISK/printer_data/gcodes/k2-plus-poopshoot-shoot-v25.stl_PLA_5h11m46s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PETG_8h57m38s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_1h32m27s.gcode
/mnt/UDISK/printer_data/gcodes/3DBenchy.stl_PLA_26m59s.gcode
/mnt/UDISK/printer_data/gcodes/race_way.stl_PLA_3h44m39s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl 3_PLA_4h53m12s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_9m27s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h8m49s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_5m32s.gcode
/mnt/UDISK/printer_data/gcodes/Component6.stl_PLA_8m22s.gcode
/mnt/UDISK/printer_data/gcodes/Parametric Hinged Box_250 mm box_Box.stl_PETG_3h22m5s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_4h58m12s.gcode
/mnt/UDISK/printer_data/gcodes/Cronos_Base.obj_PLA_1h36m28s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_6h33m14s.gcode
/mnt/UDISK/printer_data/gcodes/ROD.stl_PLA_10m57s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_15m18s.gcode
/mnt/UDISK/printer_data/gcodes/pen_head_side.stl_PLA_4h49m8s.gcode
/mnt/UDISK/printer_data/gcodes/Body6.stl_PLA_22m36s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_6h49m57s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_10m54s.gcode
/mnt/UDISK/printer_data/gcodes/yarnholder v2.stl_1_PLA_2h39m7s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_17m59s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_9m47s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_25m57s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_42m10s.gcode
/mnt/UDISK/printer_data/gcodes/Parametric_Enclosure v1.stl_1_PLA_4h0m33s.gcode
/mnt/UDISK/printer_data/gcodes/XY & Hole Compensation Test Piece.step_PLA_4m56s.gcode
/mnt/UDISK/printer_data/gcodes/lid.stl_PLA_4h0m15s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h22m35s.gcode
/mnt/UDISK/printer_data/gcodes/Bearing Spindle Part3.stl_PLA_2h57m29s.gcode
/mnt/UDISK/printer_data/gcodes/Case Bottom.stl_PLA_1h9m8s.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v5.stl_1_PLA_2h24m49s.gcode
/mnt/UDISK/printer_data/gcodes/Component5.stl_PLA_1h47m48s.gcode
/mnt/UDISK/printer_data/gcodes/StorageDrawer.stl_PLA_4h19m6s.gcode
/mnt/UDISK/printer_data/gcodes/Body8.stl_PLA_3m42s.gcode
/mnt/UDISK/printer_data/gcodes/FlexiCrystalDragon.stl_PLA_6h20m45s.gcode
/mnt/UDISK/printer_data/gcodes/digital_counter_holder.stl_PLA_1h2m13s.gcode
/mnt/UDISK/printer_data/gcodes/DuctFanAdaptor v3.stl_PLA_1h11m34s.gcode
/mnt/UDISK/printer_data/gcodes/Case.stl_PLA_1h13m28s.gcode
/mnt/UDISK/printer_data/gcodes/Full_Keycap_Test_v1_PLA_11m14s.gcode
/mnt/UDISK/printer_data/gcodes/TestBlock v1.stl_PLA_10m18s.gcode
/mnt/UDISK/printer_data/gcodes/WinderWithPulley v1.stl_4_PLA_3h25m20s.gcode
/mnt/UDISK/printer_data/gcodes/inlaytest v1.stl_1_PLA_23m58s.gcode
/mnt/UDISK/printer_data/gcodes/BallWinderCap v5.stl_PLA_23m38s.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v2.stl_PLA_18m57s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_7m22s.gcode
/mnt/UDISK/printer_data/gcodes/inlaytest v2.stl_1_PLA_17m5s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_14m19s.gcode
/mnt/UDISK/printer_data/gcodes/NASA_Fabric_Mk_3_12x16.stl_PLA_6h42m39s.gcode
/mnt/UDISK/printer_data/gcodes/WinderWithPulley v1.stl_4_PLA_24m16s.gcode
/mnt/UDISK/printer_data/gcodes/brompton_wall_mount03.stl_PLA_44m17s.gcode
/mnt/UDISK/printer_data/gcodes/Body4.stl_PLA_8m9s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_4h26m44s.gcode
/mnt/UDISK/printer_data/gcodes/3DBenchy.stl_PETG_36m4s.gcode
/mnt/UDISK/printer_data/gcodes/race_way.stl_PLA_1h25m1s.gcode
/mnt/UDISK/printer_data/gcodes/bearing_slider-p.STL_PLA_40m47s.gcode
/mnt/UDISK/printer_data/gcodes/NASA_Fabric_Mk_3_4x4.stl_PLA_8m10s.gcode
/mnt/UDISK/printer_data/gcodes/Parametric Hinged Box_250 mm box_Lid Assmebly.stl_1_PETG_1h39m40s.gcode
/mnt/UDISK/printer_data/gcodes/4mmBit.stl_PLA_6m49s.gcode
/mnt/UDISK/printer_data/gcodes/Component9.stl_PLA_1h1m31s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_4h24m55s.gcode
/mnt/UDISK/printer_data/gcodes/baseplate v1.stl_PLA_3h41m2s.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v3.stl_PLA_8m52s.gcode
/mnt/UDISK/printer_data/gcodes/k2-plus-poopshoot-shoot-v25.stl_PLA_2h15m7s.gcode
/mnt/UDISK/printer_data/gcodes/7753dec5-2d0e-42d7-a41f-af5b583a6a96.stl_PLA_7m48s.gcode
/mnt/UDISK/printer_data/gcodes/BoilerShield v8.stl_PLA_35m19s.gcode
/mnt/UDISK/printer_data/gcodes/4e9a98d4-fd7e-4f2a-9188-aa3e030161eb.stl_PLA_2h44m0s.gcode
/mnt/UDISK/printer_data/gcodes/Gear.stl_PLA_9m27s.gcode
/mnt/UDISK/printer_data/gcodes/DuctFanAdaptor v2.stl_PLA_1h43m46s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_18m17s.gcode
/mnt/UDISK/printer_data/gcodes/Knob-Insert.stl_PLA_8m19s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_18m9s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_ABS_4h15m26s.gcode
/mnt/UDISK/printer_data/gcodes/Boardcliptest v2.stl_PLA_7m9s.gcode
/mnt/UDISK/printer_data/gcodes/Component1.stl_PLA_43m13s.gcode
/mnt/UDISK/printer_data/gcodes/Body5.stl_PLA_1h20m2s.gcode
/mnt/UDISK/printer_data/gcodes/FlexiCrystalDragon_PLA_11h5m.gcode
/mnt/UDISK/printer_data/gcodes/baseplate v1.stl_PLA_2h48m37s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_6h14m14s.gcode
/mnt/UDISK/printer_data/gcodes/.e3ae3f13cc68db25035819b188e9d69e_gcode.3mf/e3ae3f13cc68db25035819b188e9d69e_gcode_plate_1.gcode
/mnt/UDISK/printer_data/gcodes/WhiteBoardBrackets.stl_1_PLA_59m50s.gcode
/mnt/UDISK/printer_data/gcodes/Awesome Spool Winder_.stl_PLA_7h28m2s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_26m51s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_2h19m17s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_6h43m46s.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v8.stl_PLA_3h7m49s.gcode
/mnt/UDISK/printer_data/gcodes/Box.stl_PETG_2h24m35s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_32m47s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_1h4m39s.gcode
/mnt/UDISK/printer_data/gcodes/pixel_pump_front_pen_rest.stl_PLA_7m58s.gcode
/mnt/UDISK/printer_data/gcodes/Body5.stl_PLA_30m5s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_10m22s.gcode
/mnt/UDISK/printer_data/gcodes/sentro_drill_adaptor.stl_PETG_31m38s.gcode
/mnt/UDISK/printer_data/gcodes/NASA_Fabric_Mk_3_8x8.stl_PLA_2h19m30s.gcode
/mnt/UDISK/printer_data/gcodes/k2-plus-poopshoot-shoot-v25.stl_PLA_2h13m41s.gcode
/mnt/UDISK/printer_data/gcodes/LaserCutterFumeExtractorAdaptor v2.stl_PLA_38m50s.gcode
/mnt/UDISK/printer_data/gcodes/iPhoneStand v4.stl_PLA_1h14m34s.gcode
/mnt/UDISK/printer_data/gcodes/ThrustBearingTemplate v2.stl_1_PLA_2h7m58s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_7h12m7s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_38m19s.gcode
/mnt/UDISK/printer_data/gcodes/K2 Plus - Chute Retainer.stl_PLA_16m54s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_31m49s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PETG_11m31s.gcode
/mnt/UDISK/printer_data/gcodes/yarnbobbin2.stl_PLA_27m9s.gcode.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_19m25s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_PLA_1h15m56s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_44m25s.gcode
/mnt/UDISK/printer_data/gcodes/Gothic-Dragon-P1lotz-FormFutura_PLA_5h40m.gcode
/mnt/UDISK/printer_data/gcodes/Worn Gear.stl_PLA_11m43s.gcode
/mnt/UDISK/printer_data/gcodes/pixel_pump_valve_junction_cap.stl_PLA_7m5s.gcode
/mnt/UDISK/printer_data/gcodes/Cube_TPU_1h42m48s.gcode
/mnt/UDISK/printer_data/gcodes/Awesome Spool Winder Motor Housing.stl_PLA_1h49m5s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_13m36s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_22m53s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h36m53s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_23m30s.gcode
/mnt/UDISK/printer_data/gcodes/25teeth gear.stl_PLA_16m18s.gcode
/mnt/UDISK/printer_data/gcodes/Whiteboard Brackets.stl_PLA_10m35s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl_PLA_4h22m49s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_1h1m58s.gcode
/mnt/UDISK/printer_data/gcodes/ScrewdriverBits v1.stl_PLA_34m33s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_2h46m30s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_2h20m11s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PETG_22m24s.gcode
/mnt/UDISK/printer_data/gcodes/Body3.stl_PLA_31m50s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_48m54s.gcode
/mnt/UDISK/printer_data/gcodes/part185109_part187446_FDM-X.stl_PLA_9h47m26s.gcode
/mnt/UDISK/printer_data/gcodes/Body9.stl_PLA_2m33s.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v7.stl_PLA_15m25s.gcode
/mnt/UDISK/printer_data/gcodes/Component2.stl_PLA_1h2m28s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_1h55m48s.gcode
/mnt/UDISK/printer_data/gcodes/race_way.stl_PLA_7h37m8s.gcode
/mnt/UDISK/printer_data/gcodes/Body75.stl_PLA_6m42s.gcode
/mnt/UDISK/printer_data/gcodes/ThrustBearingTemplate v2.stl_PLA_2h24m35s.gcode
/mnt/UDISK/printer_data/gcodes/needle-Fillet.stl_PLA_1m46s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_32m34s.gcode
/mnt/UDISK/printer_data/gcodes/Cronos_Base.obj_PLA_2h52m40s.gcode
/mnt/UDISK/printer_data/gcodes/Component5.stl_PLA_17m52s.gcode
/mnt/UDISK/printer_data/gcodes/DuctFanAdaptor v4_PLA_4h12m.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v7.stl_PLA_15m16s.gcode
/mnt/UDISK/printer_data/gcodes/Assembly_PLA_1h4m29s.gcode
/mnt/UDISK/printer_data/gcodes/yarncontainertop.stl_PLA_1h57m17s.gcode
/mnt/UDISK/printer_data/gcodes/Gothic-Dragon-P1lotz-FormFutura.stl_PLA_3h35m8s.gcode
/mnt/UDISK/printer_data/gcodes/Component7.stl_PLA_1h15m44s.gcode
/mnt/UDISK/printer_data/gcodes/NASA_Fabric_Mk_3_4x4.stl_PLA_34m43s.gcode
/mnt/UDISK/printer_data/gcodes/FlexiCrystalDragon.stl_PLA_6h20m44s.gcode
/mnt/UDISK/printer_data/gcodes/Box.stl_PLA_39m37s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_9m40s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_12m16s.gcode
/mnt/UDISK/printer_data/gcodes/Component3.stl_PLA_15m4s.gcode
/mnt/UDISK/printer_data/gcodes/Body2_PETG_25m0s.gcode
/mnt/UDISK/printer_data/gcodes/Case Bottom.stl_PLA_1h21m47s.gcode
/mnt/UDISK/printer_data/gcodes/PCBPlate.stl_PLA_29m10s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_12m9s.gcode
/mnt/UDISK/printer_data/gcodes/GiftBoxTemplate v5.stl_PLA_3h1m3s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_13m39s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_2h2m52s.gcode
/mnt/UDISK/printer_data/gcodes/Case_with_ornament.stl_PLA_2h31m59s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_8m36s.gcode
/mnt/UDISK/printer_data/gcodes/YarnSwift v10.stl_1_PLA_3h16m45s.gcode
/mnt/UDISK/printer_data/gcodes/MonitorBracket v5.stl_PLA_11m3s.gcode
/mnt/UDISK/printer_data/gcodes/Body4.stl_PLA_1h34m21s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_1h0m11s.gcode
/mnt/UDISK/printer_data/gcodes/Gothic-Dragon-P1lotz-FormFutura.stl_PLA_3h33m58s.gcode
/mnt/UDISK/printer_data/gcodes/CFS_Leg_Plug.stl_PLA_3h37m26s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PETG_14m20s.gcode
/mnt/UDISK/printer_data/gcodes/BoxLong.stl_PETG_2h55m52s.gcode
/mnt/UDISK/printer_data/gcodes/LaserCutterFumeExtractorAdaptor v4.stl_PLA_40m4s.gcode
/mnt/UDISK/printer_data/gcodes/pen_head_side.stl_PLA_4h49m49s.gcode
/mnt/UDISK/printer_data/gcodes/Ipad stand.stl_PLA_40m45s.gcode
/mnt/UDISK/printer_data/gcodes/Slider gear1.stl_PLA_1h5m22s.gcode
/mnt/UDISK/printer_data/gcodes/BoilerTrim v2.stl_1_PLA_21h21m2s.gcode
/mnt/UDISK/printer_data/gcodes/Component9.stl_1_PLA_5m38s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_49m36s.gcode
/mnt/UDISK/printer_data/gcodes/Quest_Wall_Mount_V3.85.STL_PETG_3h37m37s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_49m13s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PETG_15m12s.gcode
/mnt/UDISK/printer_data/gcodes/(Unsaved).stl_PLA_10h43m2s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_6m52s.gcode
/mnt/UDISK/printer_data/gcodes/Peggedisc.stl_PLA_13m10s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_40m43s.gcode
/mnt/UDISK/printer_data/gcodes/ScrewdriverBits v2.stl_1_PLA_17m16s.gcode
/mnt/UDISK/printer_data/gcodes/Sentro Drill Adaptor v2.stl_PETG_1h3m34s.gcode
/mnt/UDISK/printer_data/gcodes/Body268.stl_PLA_48m16s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_29m13s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PETG_10m33s.gcode
/mnt/UDISK/printer_data/gcodes/YarnSwift v4.stl_2_PLA_4h45m59s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_48m56s.gcode
/mnt/UDISK/printer_data/gcodes/Component5.stl_PLA_1h40m57s.gcode
/mnt/UDISK/printer_data/gcodes/Plate.stl_PLA_43m8s.gcode
/mnt/UDISK/printer_data/gcodes/Body2.stl_PLA_3h1m2s.gcode
/mnt/UDISK/printer_data/gcodes/3DBenchy_PLA_34m1s.gcode
/mnt/UDISK/printer_data/gcodes/Keycap ' @_PLA_20m33s.gcode
/mnt/UDISK/printer_data/gcodes/Clitoris v8.stl_PLA_14h7m41s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h44m46s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_2h56m38s.gcode
/mnt/UDISK/printer_data/gcodes/part185111_part187440_shrine-s320210105-30702-14ecif4.stl_ABS_2h58m13s.gcode
/mnt/UDISK/printer_data/gcodes/(Unsaved).stl_PLA_30m32s.gcode
/mnt/UDISK/printer_data/gcodes/Case.stl_PLA_1h3m37s.gcode
/mnt/UDISK/printer_data/gcodes/ScrewdriverBits v2.stl_PLA_11m55s.gcode
/mnt/UDISK/printer_data/gcodes/HoleTest1to8.9mmx3thk.gcode
/mnt/UDISK/printer_data/gcodes/Body4.stl_PLA_8m8s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h15m5s.gcode
/mnt/UDISK/printer_data/gcodes/FootRiser.stl_PLA_2h43m39s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_2h52m14s.gcode
/mnt/UDISK/printer_data/gcodes/3DBench_PLA_21m47s.gcode
/mnt/UDISK/printer_data/gcodes/brompton_electrical_bag_mount.stl_PLA_56m37s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_24m53s.gcode
/mnt/UDISK/printer_data/gcodes/Cronos_correction.obj_PLA_1h40m17s.gcode
/mnt/UDISK/printer_data/gcodes/Gothic-Dragon-P1lotz-FormFutura_PLA_5h31m.gcode.gcode
/mnt/UDISK/printer_data/gcodes/TriggerBoardSlot v1.stl_PLA_15m59s.gcode
/mnt/UDISK/printer_data/gcodes/guide.stl_PLA_26m57s.gcode
/mnt/UDISK/printer_data/gcodes/Body14.stl_PLA_36m47s.gcode
/mnt/UDISK/printer_data/gcodes/Body7.stl_PLA_54m19s.gcode
/mnt/UDISK/printer_data/gcodes/Gothic-Dragon-P1lotz-FormFutura_PLA_5h31m.gcode
/mnt/UDISK/printer_data/gcodes/Component5.stl_PLA_1h31m40s.gcode
/mnt/UDISK/printer_data/gcodes/clitoris_et_bulbes_3d.stl 3_PLA_52m11s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_1h12m58s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_32m15s.gcode
/mnt/UDISK/printer_data/gcodes/Body1.stl_PLA_28m16s.gcode
/mnt/UDISK/printer_data/gcodes/Drum.stl_1_PLA_59m4s.gcode
/rom/etc/sysConfig/defData/Auto_Em.gcode
/rom/etc/sysConfig/defData/Auto_pressure_advance_multi.gcode
/rom/etc/sysConfig/defData/Auto_pressure_advance_testpadvance.gcode
/rom/etc/sysConfig/defData/Auto_pressure_advance_testpadvance_product_test.gcode
/rom/etc/sysConfig/defData/auto_laser_test.gcode
/rom/etc/sysConfig/defData/laser_offset_correction.gcode
/rom/etc/sysConfig/defData/laser_offset_correction_0.2mm.gcode
/rom/etc/sysConfig/defData/laser_test_line.gcode
/rom/etc/sysConfig/defData/line_width_height.gcode
/rom/usr/share/klipper/gcodes/F008/3DBench_PLA_21m47s.gcode
/rom/usr/share/klipper/gcodes/F008/3DBenchy_PLA_34m1s.gcode
/rom/usr/share/klipper/gcodes/F008/Crealitylogo_PLA_32m41s.gcode
/rom/usr/share/klipper/gcodes/F012/3DBench_PLA_21m.gcode
/rom/usr/share/klipper/gcodes/F012/4color-3DBench_PLA_31m.gcode
/rom/usr/share/klipper/gcodes/F012/spatula_PLA_35m2s.gcode
/rom/usr/share/klipper/gcodes/F021/3DBench_PLA_22m.gcode
/rom/usr/share/klipper/gcodes/F021/4color-3DBench_PLA_32m.gcode
/rom/usr/share/klipper/gcodes/F021/spatula_PLA_34m53s.gcode
/rom/usr/share/klipper/gcodes/F025/Sermoon M300_铲刀_PLA_35m13s.gcode
/rom/usr/share/klipper/gcodes/F038/3DBench_PLA_21m.gcode
/rom/usr/share/klipper/gcodes/F038/4color-3DBench_PLA_31m.gcode
/rom/usr/share/klipper/gcodes/F038/spatula_PLA_35m2s.gcode
/rom/usr/share/klipper/gcodes/GS_01/3DBenchy_Hyper PLA_16m42s .gcode
/rom/usr/share/klipper/gcodes/GS_01/CRtestcube_Hyper PLA_26m51s.gcode
/rom/usr/share/klipper/gcodes/GS_01/Spool_holder_Hyper PLA_1H49m.gcode
/rom/usr/share/klipper/gcodes/GS_03/3DBench_PLA_21m47s.gcode
/rom/usr/share/klipper/gcodes/GS_03/3DBenchy_PLA_34m1s.gcode
/rom/usr/share/klipper/gcodes/GS_03/Crealitylogo_PLA_32m41s.gcode
/rom/usr/share/klipper/gcodes/GS_04/3DBench_PLA_21m.gcode
/rom/usr/share/klipper/gcodes/GS_04/4color-3DBench_PLA_31m.gcode
/rom/usr/share/klipper/gcodes/GS_04/spatula_PLA_35m2s.gcode
/rom/usr/share/klipper/gcodes/K1/3DBenchy.gcode
/rom/usr/share/klipper/gcodes/K1/600S-TEST-7m.gcode
/rom/usr/share/klipper/gcodes/K1/Cat.gcode
/rom/usr/share/klipper/gcodes/K1C/3DBenchy.gcode
/rom/usr/share/klipper/gcodes/K1C/600S-TEST_Hyper PLA_7m.gcode
/rom/usr/share/klipper/gcodes/K1C/Delta filament barrel base_Hyper PLA_49m.gcode
/rom/usr/share/klipper/gcodes/K1C/Logo filament barrel base_Hyper PLA_54m.gcode
/rom/usr/share/klipper/gcodes/K1_Max/3DBenchy_Hyper PLA_16m42s .gcode
/rom/usr/share/klipper/gcodes/K1_Max/CRtestcube_Hyper PLA_26m51s.gcode
/rom/usr/share/klipper/gcodes/K1_Max/K1 MAX Side Spool Holder-K1 Max_0.4_Hyper PLA_43m.gcode
/rom/usr/share/klipper/gcodes/K1_Max/Spool_holder_Hyper PLA_1H49m.gcode
/rom/usr/share/klipper/gcodes/K1_Max/scraper-K1 Max_0.4_Hyper PLA_28m.gcode
/rom/usr/share/klipper/gcodes/PF027/3DBench_PLA_21m47s.gcode
/rom/usr/share/klipper/gcodes/PF027/3DBenchy_PLA_34m1s.gcode
/rom/usr/share/klipper/gcodes/PF027/Crealitylogo_PLA_32m41s.gcode
/rom/usr/share/klipper/gcodes/Z2/3DBench_PLA_22m.gcode
/rom/usr/share/klipper/gcodes/Z2/4color-3DBench_PLA_32m.gcode
/rom/usr/share/klipper/gcodes/Z2/spatula_PLA_34m53s.gcode
/rom/usr/share/klipper/test/klippy/move.gcode
/rom/usr/share/klipper/test/klippy/sdcard_loop/big.gcode
/usr/share/klipper/gcodes/F008/3DBench_PLA_21m47s.gcode
/usr/share/klipper/gcodes/F008/3DBenchy_PLA_34m1s.gcode
/usr/share/klipper/gcodes/F008/Crealitylogo_PLA_32m41s.gcode
/usr/share/klipper/gcodes/F012/3DBench_PLA_21m.gcode
/usr/share/klipper/gcodes/F012/4color-3DBench_PLA_31m.gcode
/usr/share/klipper/gcodes/F012/spatula_PLA_35m2s.gcode
/usr/share/klipper/gcodes/F021/3DBench_PLA_22m.gcode
/usr/share/klipper/gcodes/F021/4color-3DBench_PLA_32m.gcode
/usr/share/klipper/gcodes/F021/spatula_PLA_34m53s.gcode
/usr/share/klipper/gcodes/F025/Sermoon M300_铲刀_PLA_35m13s.gcode
/usr/share/klipper/gcodes/F038/3DBench_PLA_21m.gcode
/usr/share/klipper/gcodes/F038/4color-3DBench_PLA_31m.gcode
/usr/share/klipper/gcodes/F038/spatula_PLA_35m2s.gcode
/usr/share/klipper/gcodes/GS_01/3DBenchy_Hyper PLA_16m42s .gcode
/usr/share/klipper/gcodes/GS_01/CRtestcube_Hyper PLA_26m51s.gcode
/usr/share/klipper/gcodes/GS_01/Spool_holder_Hyper PLA_1H49m.gcode
/usr/share/klipper/gcodes/GS_03/3DBench_PLA_21m47s.gcode
/usr/share/klipper/gcodes/GS_03/3DBenchy_PLA_34m1s.gcode
/usr/share/klipper/gcodes/GS_03/Crealitylogo_PLA_32m41s.gcode
/usr/share/klipper/gcodes/GS_04/3DBench_PLA_21m.gcode
/usr/share/klipper/gcodes/GS_04/4color-3DBench_PLA_31m.gcode
/usr/share/klipper/gcodes/GS_04/spatula_PLA_35m2s.gcode
/usr/share/klipper/gcodes/K1/3DBenchy.gcode
/usr/share/klipper/gcodes/K1/600S-TEST-7m.gcode
/usr/share/klipper/gcodes/K1/Cat.gcode
/usr/share/klipper/gcodes/K1C/3DBenchy.gcode
/usr/share/klipper/gcodes/K1C/600S-TEST_Hyper PLA_7m.gcode
/usr/share/klipper/gcodes/K1C/Delta filament barrel base_Hyper PLA_49m.gcode
/usr/share/klipper/gcodes/K1C/Logo filament barrel base_Hyper PLA_54m.gcode
/usr/share/klipper/gcodes/K1_Max/3DBenchy_Hyper PLA_16m42s .gcode
/usr/share/klipper/gcodes/K1_Max/CRtestcube_Hyper PLA_26m51s.gcode
/usr/share/klipper/gcodes/K1_Max/K1 MAX Side Spool Holder-K1 Max_0.4_Hyper PLA_43m.gcode
/usr/share/klipper/gcodes/K1_Max/Spool_holder_Hyper PLA_1H49m.gcode
/usr/share/klipper/gcodes/K1_Max/scraper-K1 Max_0.4_Hyper PLA_28m.gcode
/usr/share/klipper/gcodes/PF027/3DBench_PLA_21m47s.gcode
/usr/share/klipper/gcodes/PF027/3DBenchy_PLA_34m1s.gcode
/usr/share/klipper/gcodes/PF027/Crealitylogo_PLA_32m41s.gcode
/usr/share/klipper/gcodes/Z2/3DBench_PLA_22m.gcode
/usr/share/klipper/gcodes/Z2/4color-3DBench_PLA_32m.gcode
/usr/share/klipper/gcodes/Z2/spatula_PLA_34m53s.gcode
/usr/share/klipper/test/klippy/move.gcode
/usr/share/klipper/test/klippy/sdcard_loop/big.gcode
