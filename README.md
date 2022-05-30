# KitKat
adb push path/to/mtk-su /data/local/tmp/
adb shell
cd /data/local/tmp
chmod 755 mtk-su
./mtk-su
mount -o remount,rw /system
cp /data/local/tmp/mtk-su /system/bin/su
dd if=/dev/block/bootdevice/by-name/boot of=/sdcard/boot.img
dd if=/dev/block/bootdevice/by-name/recovery of=/sdcard/recovery.img
