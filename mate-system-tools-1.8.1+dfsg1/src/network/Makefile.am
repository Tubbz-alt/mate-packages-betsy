##
## Process this file with automake to produce Makefile.in
##
## Please don't modify this file unless you know what you are doing
## Please keep the Makefile.am from all the tools in sync
##

include ../common/CommonMakefile

toolname = mate-network
bin_PROGRAMS = mate-network-admin

## SUBDIRS =
AM_CPPFLAGS += $(GST_TOOL_CFLAGS) $(DBUS_CFLAGS) $(GIO_CFLAGS)
CLEANFILES = $(GST_TOOL_CLEANFILES)
EXTRA_DIST = $(GST_TOOL_EXTRA_DIST)

mate_network_admin_LDADD = $(GST_TOOL_LIBS) $(GST_IW_LIBS) $(DBUS_LIBS) $(GIO_LIBS)
mate_network_admin_DEPENDENCIES = $(GST_TOOL_DEPENDENCIES)

if HAVE_LIBIW_H
essid_SOURCES = essid-list.c essid-list.h
endif

mate_network_admin_SOURCES = \
	$(essid_SOURCES) \
	nm-integration.c \
	nm-integration.h \
	address-list.c \
	address-list.h \
	network-locations.c \
	network-locations.h \
	network-tool.c \
	network-tool.h \
	locations-combo.c \
	locations-combo.h \
	ifaces-list.c \
	ifaces-list.h \
	callbacks.c \
	callbacks.h \
	connection.c \
	connection.h \
	hosts.c hosts.h \
	main.c

toolpixmaps =

-include $(top_srcdir)/git.mk
