# 
# Copyright (C) 2006-2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/target.mk

PKG_NAME:=ccache
PKG_VERSION:=3.1.7

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_SOURCE_URL:=http://samba.org/ftp/ccache/
PKG_MD5SUM:=80a698c22d0b06b19c88ac58e8d8b632
PKG_CAT:=zcat

include $(INCLUDE_DIR)/host-build.mk

ifneq ($(strip $(shell which ccache >/dev/null && echo found)),found)
  define Host/Compile
	$(MAKE) CC="$(HOSTCC_NOCACHE)" -C $(HOST_BUILD_DIR)
  endef

  define Host/Clean
	-$(MAKE) -C $(HOST_BUILD_DIR) uninstall
	$(call Host/Clean/Default)
  endef
else
  define Host/Prepare
  endef
  define Host/Configure
  endef
  define Host/Compile
  endef
  define Host/Install
  endef
  define Host/Clean
  endef
  define Download
  endef
endif

$(eval $(call HostBuild))
