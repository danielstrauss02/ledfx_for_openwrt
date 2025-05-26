#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-ninja
PKG_VERSION:=1.11.1.4
PKG_RELEASE:=1

PYPI_NAME:=ninja
PKG_HASH:=6aa39f6e894e0452e5b297327db00019383ae55d5d9c57c73b04f13bf79d438a

PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE_Apache_20
PKG_MAINTAINER:=

PKG_HOST_ONLY:=1
HOST_BUILD_DEPENDS:=python3/host python-scikit-build-core/host python-hatch-fancy-pypi-readme/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include ../../packages/lang/python/python3-package.mk
include ../../packages/lang/python/python3-host-build.mk

define Package/python-ninja
  CATEGORY:=LedFx for OpenWrt
  TITLE:=Ninja is a small build system with a focus on speed
  URL:=https://ninja-build.org/
  BUILDONLY:=1
endef

define Package/python-ninja/description
Ninja is a small build system with a focus on speed.
endef

$(eval $(call Py3Package,python-ninja))
$(eval $(call BuildPackage,python-ninja))
$(eval $(call BuildPackage,python-ninja-src))
$(eval $(call HostBuild))
