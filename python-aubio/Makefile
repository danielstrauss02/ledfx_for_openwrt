#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=aubio
PKG_VERSION:=0.4.9
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=df1244f6c4cf5bea382c8c2d35aa43bc31f4cf631fe325ae3992c219546a4202

PKG_LICENSE:=GPL-3.0
PKG_LICENSE_FILES:=COPYING
PKG_MAINTAINER:=

HOST_BUILD_DEPENDS:=python3/host python3-numpy-1.26.4/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk

define Package/python-aubio
  CATEGORY:=LedFx for OpenWrt
  TITLE:=A collection of tools for music analysis
  URL:=https://aubio.org/
  DEPENDS:=+python3 +python3-numpy-1.26.4
endef

define Package/python-aubio/description
aubio is a tool designed for the extraction of annotations from audio signals. 
endef

$(eval $(call Py3Package,python-aubio))
$(eval $(call BuildPackage,python-aubio))
$(eval $(call BuildPackage,python-aubio-src))