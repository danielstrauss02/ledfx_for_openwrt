#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=meson-python
PKG_VERSION:=0.18.0
PKG_RELEASE:=1

PYPI_NAME:=meson_python
PKG_HASH:=c56a99ec9df669a40662fe46960321af6e4b14106c14db228709c1628e23848d

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=

PKG_HOST_ONLY:=1
HOST_BUILD_DEPENDS:=python3/host pyproject-metadata/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include ../../packages/lang/python/python3-package.mk
include ../../packages/lang/python/python3-host-build.mk

define Package/meson-python
  CATEGORY:=LedFx for OpenWrt
  TITLE:=Meson Python build backend (PEP 517)
  URL:=https://mesonbuild.com/meson-python/
  BUILDONLY:=1
endef

define Package/meson-python/description
meson-python is a Python build back-end built on top of the Meson build system. 
It enables using Meson for the configuration and build steps of Python packages. 
Meson is an open source build system meant to be both extremely fast, and, 
even more importantly, as user friendly as possible.
endef

$(eval $(call Py3Package,meson-python))
$(eval $(call BuildPackage,meson-python))
$(eval $(call BuildPackage,meson-python-src))
$(eval $(call HostBuild))
