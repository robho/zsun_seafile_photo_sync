# Zsun seafile photo sync

Here are some scripts to use a zsun WiFi SD card reader to sync photos
from a Seafile repository to a digital photo frame.

There's also some code to shuffle the images by randomizing the file
names. This is useful to me because my photo frame's implementation of
random display order is very deterministic.


# Installation instructions

Install OpenWrt / LEDE to the wifi card reader. See:
* https://wiki.hackerspace.pl/projects:zsun-wifi-card-reader
* https://forum.lede-project.org/t/supporting-zsun-wifi-card-reader-16mb-flash-64mb-ram-ar9331/2142/71

Install additional OpenWrt packages. These can be fetched from the
LEDE repositories:

block-mount
coreutils
coreutils-shuf
coreutils-stat
curl
dosfstools
libcurl
libmbedtls

These you can extract from the image builder archive:
kmod-fs-vfat
kmod-nls-base
kmod-nls-cp437
kmod-nls-iso8859-1
kmod-nls-utf8
kmod-scsi-core
kmod-usb-core
kmod-usb-storage
kmod-usb2

Next, copy the scripts to your zsun device, update the configuration
and set up a cron job or init script to download and shuffle the
images.