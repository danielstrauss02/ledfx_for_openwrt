#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=sacn
PKG_VERSION:=1.11.0
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=148b39ca7f3dd616878a70a62b7410d094080977e784f8a6302f352d7395e0ea

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=

HOST_BUILD_DEPENDS:=python3/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk

define Package/python-sacn
  CATEGORY:=LedFx for OpenWrt
  TITLE:=sACN / E1.31 module for easy handling of DMX data over ethernet
  URL:=https://github.com/Hundemeier/sacn
  DEPENDS:=+python3
endef

define Package/python-sacn/description
This module is a simple sACN library that support the standard DMX message
of the protocol. It is based on the 2016 version of the official ANSI E1.31
standard. It has support for sending out DMX data and receiving it. 
Multiple and multicast universes are supported.
endef

$(eval $(call Py3Package,python-sacn))
$(eval $(call BuildPackage,python-sacn))
$(eval $(call BuildPackage,python-sacn-src))
