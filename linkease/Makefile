include $(TOPDIR)/rules.mk

PKG_NAME:=linkease
PKG_RELEASE:=1
PKG_VERSION=2.0

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/version.mk

WEB_PATH:=www

define Build/Prepare
	echo -e "all:\n\techo 'jiajiaclient ok'" > "$(PKG_BUILD_DIR)/Makefile"
endef

define Package/linkease/default
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Web Servers/Proxies
  TITLE:=linkease
endef

define Package/linkease
  $(Package/linkease/default)
endef

define Package/linkease/description
  linkease file cloud
endef

define Package/linkease/postinst
#!/bin/sh
if [ -z $${IPKG_INSTROOT} ]; then
	/etc/init.d/linkease enable
fi
endef

define Package/linkease/install
	install -d -m0755 $(1)/etc/{init.d,config} $(1)/sbin
	install -m0755 ./files/linkease.init $(1)/etc/init.d/linkease
	install -m0755 ./files/link-ease $(1)/sbin/
	install -m0755 ./files/linkease-monitor $(1)/sbin/
endef

$(eval $(call BuildPackage,linkease))
