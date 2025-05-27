#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-rtmidi
PKG_VERSION:=1.5.8
PKG_RELEASE:=1

PYPI_NAME:=python_rtmidi
PKG_HASH:=7f9ade68b068ae09000ecb562ae9521da3a234361ad5449e83fc734544d004fa

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.md
PKG_MAINTAINER:=

HOST_BUILD_DEPENDS:=python3/host meson-python/host python-cython/host

MESON_USE_STAGING_PYTHON:=1

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/python/python3-package.mk
include $(INCLUDE_DIR)/meson.mk

define Package/python-rtmidi
  CATEGORY:=LedFx for OpenWrt
  TITLE:=A Python binding for the RtMidi C++ library implemented using Cython.
  URL:=https://spotlightkid.github.io/python-rtmidi/
  DEPENDS:=+python3 +alsa-lib +libstdcpp
endef

define Package/python-rtmidi/description
RtMidi is a set of C++ classes which provides a concise and simple, cross-platform 
API (Application Programming Interface) for realtime MIDI input / output.
endef

$(eval $(call Py3Package,python-rtmidi))
$(eval $(call BuildPackage,python-rtmidi))
$(eval $(call BuildPackage,python-rtmidi-src))
