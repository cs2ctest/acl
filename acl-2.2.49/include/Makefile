#
# Copyright (c) 2001-2002 Silicon Graphics, Inc.  All Rights Reserved.
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307 USA
#

TOPDIR = ..
include $(TOPDIR)/include/builddefs

HFILES = acl.h libacl.h acl_ea.h misc.h walk_tree.h
LSRCFILES = builddefs.in buildmacros buildrules config.h.in install-sh
LDIRT = sys acl

default: sys acl

sys acl:
	$(LN_S) . $@

include $(BUILDRULES)

install-dev: default
	$(INSTALL) -m 755 -d $(PKG_INC_DIR)
	$(INSTALL) -m 755 -d $(PKG_INC_DIR)/sys
	$(INSTALL) -m 644 acl.h $(PKG_INC_DIR)/sys/acl.h
	$(INSTALL) -m 755 -d $(PKG_INC_DIR)/acl
	$(INSTALL) -m 644 libacl.h $(PKG_INC_DIR)/acl/libacl.h

install install-lib:
