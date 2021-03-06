#
# Copyright (C) Alexandru Ardelean <ardeleanalex@gmail.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=django1
PKG_VERSION:=1.11.28
PKG_RELEASE:=1

PYPI_NAME:=Django
PKG_HASH:=b33ce35f47f745fea6b5aa3cf3f4241069803a3712d423ac748bd673a39741eb

PKG_MAINTAINER:=Alexandru Ardelean <ardeleanalex@gmail.com>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE LICENSE.python
PKG_CPE_ID:=cpe:/a:djangoproject:django

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python-package.mk

define Package/django1/Default
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=The web framework for perfectionists with deadlines.
  URL:=https://www.djangoproject.com/
  MENU:=1
endef

define Package/python-django1
$(call Package/django1/Default)
  DEPENDS:= \
	+PACKAGE_python-django1:python \
	+PACKAGE_python-django1:python-pytz
  VARIANT:=python
  CONFLICTS:=python3-django
endef

define Package/python-django1/description
    The web framework for perfectionists with deadlines (LTS 1.11 series).
    Python2 only.
endef

$(eval $(call PyPackage,python-django1))
define Package/python-django1-src +=

  MDEPENDS:=python-django1
endef
$(eval $(call BuildPackage,python-django1))
$(eval $(call BuildPackage,python-django1-src))
