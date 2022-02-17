# rpi-cm4-archlinuxarm-aarch64-boot
Working eMMC /boot directory on a Raspberry PI CM4 module that runs ArchLinux ARM aarch64 - 5.16.8-1-aarch64-ARCH

Make sure that you modify cmdline.txt so that it points to the correct ROOT file system.
Plug in a serial cable (FTDI) and monitor with a baud rate: 115200, if you are having trouble booting up. This will allow you to debug even with no disply out.

Modify config.txt as you wish.
Current settings are:
gpu_mem=64
initramfs initramfs-linux.img followkernel
kernel=Image
arm_64bit=1
disable_overscan=1
watchdog=on

#enable sound
#dtparam=audio=on
#hdmi_drive=2
hdmi_blanking=2

#enable vc4
#dtoverlay=dwc2,dr_mode=host,vc4-fkms-v3d
dtoverlay=pi3-disable-bt,pi3-disable-wifi
max_framebuffers=2
disable_splash=1

#uart for cm4
uart_2ndstage=1
enable_uart=1
