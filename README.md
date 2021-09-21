# Zsun seafile photo sync

Here are some scripts to use a zsun WiFi SD card reader to sync photos
from a Seafile repository to a digital photo frame.

Connect the zsun device (with an SD card installed) to the photo frame's
USB port, install these scripts and update the configuration.
The scripts will download, resize, rotate and shuffle images and then
expose the SD card as a USB storage device to the photo frame.


# Installation instructions

Install OpenWrt 21.02.0 to the wifi card reader. See:
* https://wiki.hackerspace.pl/projects:zsun-wifi-card-reader
* https://github.com/brunompena/zsun-resources

Install additional OpenWrt packages:
* coreutils-shuf
* coreutils-stat
* dosfstools
* graphicsmagick
* kmod-fs-vfat

Next, copy the scripts to your zsun device, update the configuration
and set up a cron job or init script to download and shuffle the
images.
