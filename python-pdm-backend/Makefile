#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-pdm-backend
PKG_VERSION:=2.4.4
PKG_RELEASE:=1

PYPI_NAME:=pdm_backend
PKG_HASH:=f72551eeb319f74ca25856c24fb4026684eeb0dddd9df68482901ab0dc481258

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=

PKG_HOST_ONLY:=1
HOST_BUILD_DEPENDS:=python3/host python-build/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include ../../packages/lang/python/python3-package.mk
include ../../packages/lang/python/python3-host-build.mk

define Package/python-pdm-backend
  CATEGORY:=LedFx for OpenWrt
  TITLE:=The build backend used by PDM that supports latest packaging standards
  URL:=https://backend.pdm-project.org/
  BUILDONLY:=1
endef

define Package/python-pdm-backend/description
This is the backend for PDM projects that is fully-compatible with PEP 517 spec, 
but you can also use it alone. It reads the metadata of PEP 621 format and 
coverts it to Core metadata.
endef

$(eval $(call Py3Package,python-pdm-backend))
$(eval $(call BuildPackage,python-pdm-backend))
$(eval $(call BuildPackage,python-pdm-backend-src))
$(eval $(call HostBuild))
