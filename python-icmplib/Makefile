#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=icmplib
PKG_VERSION:=3.0.4
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=57868f2cdb011418c0e1d5586b16d1fabd206569fe9652654c27b6b2d6a316de

PKG_LICENSE:=LGPL-3.0
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=

HOST_BUILD_DEPENDS:=python3/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk

define Package/python-icmplib
  CATEGORY:=LedFx for OpenWrt
  TITLE:=Easily forge ICMP packets and make your own ping and traceroute.
  URL:=https://github.com/ValentinBELYN/icmplib
  DEPENDS:=+python3
endef

define Package/python-icmplib/description
icmplib is a brand new and modern implementation of the ICMP protocol in Python.
Use the built-in functions or build your own, you have the choice!
endef

$(eval $(call Py3Package,python-icmplib))
$(eval $(call BuildPackage,python-icmplib))
$(eval $(call BuildPackage,python-icmplib-src))
