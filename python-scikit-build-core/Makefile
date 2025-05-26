#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-scikit-build-core
PKG_VERSION:=0.11.3
PKG_RELEASE:=1

PYPI_NAME:=scikit_build_core
PKG_HASH:=74baf7cbc089f8621cc0646d9c5679034d5be1b014c10912dc32a4bcd1092506

PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=

PKG_HOST_ONLY:=1
HOST_BUILD_DEPENDS:=python3/host python-hatchling/host python-packaging/host python-hatch-vcs/host

include ../../packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include ../../packages/lang/python/python3-package.mk
include ../../packages/lang/python/python3-host-build.mk

define Package/python-scikit-build-core
  CATEGORY:=LedFx for OpenWrt
  TITLE:=Build backend for CMake based projects
  URL:=https://scikit-build-core.readthedocs.io/
  BUILDONLY:=1
endef

define Package/python-scikit-build-core/description
Scikit-build-core is a build backend for Python that uses CMake to build 
extension modules. It has a simple yet powerful static configuration system 
in pyproject.toml, and supports almost unlimited flexibility via CMake.
endef

$(eval $(call Py3Package,python-scikit-build-core))
$(eval $(call BuildPackage,python-scikit-build-core))
$(eval $(call BuildPackage,python-scikit-build-core-src))
$(eval $(call HostBuild))
