include $(TOPDIR)/rules.mk

PKG_NAME:=libbabelhelper

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ffgraz/libbabelhelper.git
PKG_SOURCE_DATE:=2026-08-24
PKG_SOURCE_VERSION:=5705edc96206b16b42fdf2a15d48f29a433a9549

CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/libbabelhelper
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=Babel utility library
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/libbabelhelper-* $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libbabelhelper.so* $(1)/usr/lib/
	$(INSTALL_DIR) $(1)/usr/lib/pkgconfig
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/libbabelhelper.pc $(1)/usr/lib/pkgconfig/
endef


define Package/libbabelhelper/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/libbabelhelper.so* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libbabelhelper))
