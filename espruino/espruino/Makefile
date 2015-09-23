#
# Copyright (C) 2006-2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=espruino
PKG_VERSION:=1.80.0-git
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/espruino/Espruino.git
PKG_SOURCE_VERSION:=44f2fc15e94e3eac6cb0cbd908b66ec8886e9d88
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_MIRROR_MD5SUM:=66a728a3cb8dad0e3773035c4049eb5f

include $(INCLUDE_DIR)/package.mk

define Package/espruino
  SUBMENU:=JavaScript
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=A compact JavaScript interpreter
  URL:=http://www.espruino.com
  DEPENDS:=+libpthread +librt +uclibcxx
endef

define Package/espruino/description
 Espruino is an extremely compact JavaScript interpreter. Originally
 designed for microcontrollers, it runs on OpenWRT while using a very small
 amount of RAM. It includes a cut-down version of node's HTTP client and
 server, filesystem, as well as GPIO support.
endef

MAKE_FLAGS += \
	LD="$(TARGET_CC)" \
	RELEASE=1 V=1

define Package/espruino/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/espruino $(1)/usr/bin/
endef

$(eval $(call BuildPackage,espruino))
