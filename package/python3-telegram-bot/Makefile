include $(TOPDIR)/rules.mk

PKG_NAME:=python3-telegram-bot
PKG_VERSION:=22.1
PKG_RELEASE:=1

PYPI_NAME:=python-telegram-bot
PKG_HASH:=skip

PKG_LICENSE:=LGPL-3.0
PKG_MAINTAINER:=You <you@example.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PYPI_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/python3-package.mk

define Package/python3-telegram-bot
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Python Telegram Bot library
  URL:=https://python-telegram-bot.org/
  DEPENDS:= \
    +python3 \
    +python3-logging \
    +python3-ssl \
    +python3-urllib \
    +python3-certifi \
    +python3-idna \
    +python3-charset-normalizer \
    +python3-requests \
    +python3-httpx \
    +python3-typing-extensions
endef

define Package/python3-telegram-bot/description
 Modern, fully asynchronous Python framework for Telegram Bot API.
endef

# ====== PENTING: FIX CLEAN TARGET ======
define Build/Clean
	rm -rf $(PKG_BUILD_DIR)
endef

define Build/Compile
	$(call Py3Build/Compile)
endef

define Package/python3-telegram-bot/install
	$(call Py3Package/install,$(1))
endef

$(eval $(call BuildPackage,python3-telegram-bot))
