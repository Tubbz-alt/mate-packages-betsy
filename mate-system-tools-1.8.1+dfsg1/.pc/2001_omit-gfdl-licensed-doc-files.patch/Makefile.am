SUBDIRS = doc icons interfaces pixmaps src po

distuninstallcheck_listfiles = find . -type f -print | grep -v scrollkeeper

EXTRA_DIST = \
	HACKING \
	BUGS \
	intltool-extract.in \
	intltool-merge.in \
	intltool-update.in \
	omf.make \
	xmldocs.make \
	mate-system-tools.pc.in \
	org.mate.system-tools.gschema.xml.in

gsettings_SCHEMAS = org.mate.system-tools.gschema.xml
@GSETTINGS_RULES@
@INTLTOOL_XML_NOMERGE_RULE@

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = mate-system-tools.pc

DISTCLEANFILES = \
	intltool-extract \
	intltool-merge \
	intltool-update \
	backends/intltool-extract \
	backends/intltool-merge \
	backends/intltool-update \
	mate-system-tools.pc \
	org.mate.system-tools.gschema.xml

MAINTAINERCLEANFILES = \
	INSTALL \
	aclocal.m4 \
	config.guess \
	config.h.in \
	config.sub \
	depcomp \
	install-sh \
	ltmain.sh \
	missing \
	mkinstalldirs \
	omf.make \
	xmldocs.make \
	`find "$(srcdir)" -type f -name Makefile.in -print`

DISTCHECK_CONFIGURE_FLAGS = --disable-scrollkeeper --with-cajadir='$${libdir}/caja/extensions-2.0-distcheck'

-include $(top_srcdir)/git.mk
