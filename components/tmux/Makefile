#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"). You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2011, 2013, EveryCity Ltd. All rights reserved.
#

include ../../make-rules/shared-macros.mk

COMPONENT_NAME=		tmux
COMPONENT_VERSION=	2.0
COMPONENT_REVISION=	1
COMPONENT_PROJECT_URL=	http://$(COMPONENT_NAME).sourceforge.net
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	sha256:795f4b4446b0ea968b9201c25e8c1ef8a6ade710ebca4657dd879c35916ad362
COMPONENT_ARCHIVE_URL=	http://downloads.sourceforge.net/$(COMPONENT_NAME)/$(COMPONENT_ARCHIVE)

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/deb.mk

CFLAGS +=	-I/usr/include/ncurses

CONFIGURE_OPTIONS +=	LIBS="-lncurses"

build:		$(DEFAULT_BUILD)

install:	$(DEFAULT_INSTALL)

include $(WS_MAKE_RULES)/depend.mk
