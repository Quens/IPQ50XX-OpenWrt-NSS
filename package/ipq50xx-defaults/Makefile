# SPDX-License-Identifier: GPL-2.0-only
#
# First-boot defaults of every ipq50xx image: the LAN subnet, Wi-Fi
# defaults and region the H3C QSDK images ship, applied to every board of
# the build rather than to the H3C Magic boards alone, and a Chinese LuCI.

include $(TOPDIR)/rules.mk

PKG_NAME:=ipq50xx-defaults
PKG_RELEASE:=1
PKG_LICENSE:=GPL-2.0-only

include $(INCLUDE_DIR)/package.mk

define Package/ipq50xx-defaults
  SECTION:=base
  CATEGORY:=Base system
  TITLE:=First-boot defaults for the ipq50xx NSS images
  DEPENDS:=@TARGET_qualcommax_ipq50xx
  PKGARCH:=all
endef

define Package/ipq50xx-defaults/description
 For a fresh configuration on any board of the ipq50xx target, whatever
 the model: LAN 192.168.10.1, hostname OpenWrt, both Wi-Fi bands up with
 WPA2 (OpenWrt / OpenWrt-5G, key 12345678), country CN, time zone
 Asia/Shanghai with NTP servers in China, and LuCI in Simplified Chinese.
 A keep-settings sysupgrade keeps the user's network, Wi-Fi and LuCI
 settings.
endef

define Build/Compile
endef

define Package/ipq50xx-defaults/install
	$(INSTALL_DIR) $(1)/etc/board.d $(1)/etc/uci-defaults
	$(INSTALL_DATA) ./files/etc/board.d/99_ipq50xx_defaults $(1)/etc/board.d/
	$(INSTALL_BIN) ./files/etc/uci-defaults/99-ipq50xx-defaults $(1)/etc/uci-defaults/
endef

$(eval $(call BuildPackage,ipq50xx-defaults))
