#
# Copyright (c) 2016 Thorsten Kukuk, Germany
#
# Author: Thorsten Kukuk <kukuk@suse.de>
#

CLEANFILES = $(MANS)

EXTRA_DIST = $(MANS) $(XMLS)

man_MANS = rebootmgrd.8 rebootmgr-dbus.conf.8 rebootmgr.service.8
XMLS = rebootmgrd.8.xml

if ENABLE_REGENERATE_MAN
rebootmgrd.8: rebootmgrd.8.xml
	$(XMLLINT) --nonet --xinclude --postvalid --noout $<
	$(XSLTPROC) -o $(srcdir)/$@ --path $(srcdir) --xinclude --nonet http://docbook.sourceforge.net/release/xsl/current/manpages/docbook.xsl $<
endif
