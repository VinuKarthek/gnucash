SUBDIRS = . gschemas test

pkglib_LTLIBRARIES=libgncmod-ofx.la

libgncmod_ofx_la_SOURCES = \
  gnc-ofx-import.c \
  gnc-ofx-kvp.c \
  gncmod-ofx-import.c \
  gnc-plugin-ofx.c

noinst_HEADERS = \
  gnc-ofx-import.h \
  gnc-ofx-kvp.h \
  gnc-plugin-ofx.h

libgncmod_ofx_la_LDFLAGS = -avoid-version

libgncmod_ofx_la_LIBADD = \
  ${top_builddir}/gnucash/import-export/libgncmod-generic-import.la \
  ${top_builddir}/gnucash/gnome-utils/libgncmod-gnome-utils.la \
  ${top_builddir}/libgnucash/app-utils/libgncmod-app-utils.la \
  ${top_builddir}/libgnucash/engine/libgncmod-engine.la \
  ${top_builddir}/libgnucash/core-utils/libgnc-core-utils.la \
  ${top_builddir}/libgnucash/gnc-module/libgnc-module.la \
  ${GLIB_LIBS} \
  ${LIBOFX_LIBS}

AM_CPPFLAGS = \
  -I${top_srcdir}/common \
  -I${top_srcdir}/libgnucash/core-utils \
  -I${top_srcdir}/libgnucash/engine \
  -I${top_srcdir}/libgnucash/gnc-module \
  -I${top_srcdir}/libgnucash/app-utils \
  -I${top_srcdir}/gnucash/gnome \
  -I${top_srcdir}/gnucash/gnome-utils \
  -I${top_srcdir}/gnucash/import-export \
  ${GTK_CFLAGS} \
  ${GLIB_CFLAGS} \
  ${LIBOFX_CFLAGS} 

uidir = $(GNC_UI_DIR)
ui_DATA = \
	gnc-plugin-ofx-ui.xml

EXTRA_DIST = $(ui_DATA) migratable-prefs-ofx.xml CMakeLists.txt

AM_CPPFLAGS += -DG_LOG_DOMAIN=\"gnc.import.ofx\"
