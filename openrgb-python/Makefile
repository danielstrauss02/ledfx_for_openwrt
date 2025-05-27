#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=openrgb-python
PKG_VERSION:=0.3.3
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=5d09f161fb3b568b8004134183b9974f75c67db10fdcf359cd53bc4e54e94947

PKG_LICENSE:=GPL-3.0
PKG_LICENSE_FILES:=
PKG_MAINTAINER:=

HOST_BUILD_DEPENDS:=python3/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk

define Package/openrgb-python
  CATEGORY:=LedFx for OpenWrt
  TITLE:=A python client for the OpenRGB SDK
  URL:=https://github.com/jath03/openrgb-python
  DEPENDS:=+python3
endef

define Package/openrgb-python/description
OpenRGB-Python is a client for the OpenRGB SDK, a manufacturer-independent, 
cross-platform way to control your RGB devices. OpenRGB-Python can be used 
to interface with other programs, create custom effects, or anything else 
you can think of!
endef

$(eval $(call Py3Package,openrgb-python))
$(eval $(call BuildPackage,openrgb-python))
$(eval $(call BuildPackage,openrgb-python-src))
