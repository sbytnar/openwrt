# 
# Copyright (C) 2006-2010 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=at91
MAINTAINER:=Claudio Mignanti <c.mignanti@gmail.com>
BOARDNAME:=Atmel AT91
FEATURES:=squashfs jffs2 targz ext2 usb
CFLAGS:=-Os -pipe -march=armv5te -mtune=arm926ej-s -fno-caller-saves
SUBTARGETS:=9g20 9260 9263

LINUX_VERSION:=3.3.5
DEVICE_TYPE=

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES+= kmod-usb-ohci
KERNELNAME:="uImage"

$(eval $(call BuildTarget))
