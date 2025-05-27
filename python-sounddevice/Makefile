#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=sounddevice
PKG_VERSION:=0.5.2
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=c634d51bd4e922d6f0fa5e1a975cc897c947f61d31da9f79ba7ea34dff448b49

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=

HOST_BUILD_DEPENDS:=python3/host python-cffi/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk

define Package/python-sounddevice
  CATEGORY:=LedFx for OpenWrt
  TITLE:=Play and Record Sound with Python
  URL:=https://python-sounddevice.readthedocs.io
  DEPENDS:=+python3 +python3-cffi
endef

define Package/python-sounddevice/description
This Python module provides bindings for the PortAudio library and a few 
convenience functions to play and record NumPy arrays containing audio signals.
endef

$(eval $(call Py3Package,python-sounddevice))
$(eval $(call BuildPackage,python-sounddevice))
$(eval $(call BuildPackage,python-sounddevice-src))
