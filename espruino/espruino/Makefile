include $(TOPDIR)/rules.mk

PKG_NAME:=espruino
PKG_VERSION:=1.94.0-git
PKG_RELEASE:=1

PKG_MAINTAINER:=Volodymyr Shymanskyy
PKG_LICENSE:=MIT

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/espruino/Espruino.git
PKG_SOURCE_VERSION:=RELEASE_1V94
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/espruino
  SUBMENU:=JavaScript
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=A compact JavaScript interpreter
  URL:=http://www.espruino.com
  DEPENDS:=+libpthread
endef

define Package/espruino/description
 Espruino is an extremely compact JavaScript interpreter. Originally
 designed for microcontrollers, it runs on OpenWRT while using a very small
 amount of RAM.
endef

MAKE_FLAGS += LD="$(TARGET_CC)"
MAKE_FLAGS += RELEASE=1
MAKE_FLAGS += OPENWRT_UCLIBC=1

define Package/espruino/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/espruino $(1)/usr/bin/
endef

$(eval $(call BuildPackage,espruino))
