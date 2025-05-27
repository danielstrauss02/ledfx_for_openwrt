#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ledfx
PKG_VERSION:=2.0.108
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=c1fa7abb6608962b9f8e468b0652d5170dbf76aa4760501f728c388b2381d8c1

PKG_LICENSE:=GPL-3.0
PKG_LICENSE_FILES:=LICENSE.txt
PKG_MAINTAINER:=

HOST_BUILD_DEPENDS:=python3/host python-pdm-backend/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk

define Package/ledfx
  CATEGORY:=LedFx for OpenWrt
  TITLE:=A network based light effect controller
  URL:=https://ledfx.app
  DEPENDS:=+python3 +python-rtmidi
endef

define Package/ledfx/description
LedFx makes your LEDs dance to audio! What LedFx offers is the ability 
to take audio input, and instantaneously processes the audio into realtime 
light show to multiple LED strips/matrix. 
endef

$(eval $(call Py3Package,ledfx))
$(eval $(call BuildPackage,ledfx))
$(eval $(call BuildPackage,ledfx-src))
