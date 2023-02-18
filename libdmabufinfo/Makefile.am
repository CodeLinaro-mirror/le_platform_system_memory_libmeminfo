AM_CPPFLAGS := \
    -W \
    -Wall \
    -Wextra \
    -Wunused \
    -Wno-missing-field-initializers

ACLOCAL_AMFLAGS = -I m4

SUBDIRS = .  tools


# Build libdmabufinfo.so
libdmabufinfo_sources = dmabufinfo.cpp dmabuf_sysfs_stats.cpp
lib_LTLIBRARIES = libdmabufinfo.la

libdmabufinfo_la_SOURCES = $(libdmabufinfo_sources)
libdmabufinfo_la_CPPFLAGS = -I$(top_srcdir)/include
libdmabufinfo_la_CPPFLAGS += $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
libdmabufinfo_la_CPPFLAGS += -std=c++17
libdmabufinfo_la_CPPFLAGS += -I$(srcdir)/include

libdmabufinfo_la_CPPFLAGS += @LIBBASE_CFLAGS@ @LIBION_CFLAGS@
libdmabufinfo_la_LDFLAGS = @LIBBASE_LIBS@ @LIBION_LIBS@  -lion

# Export headers
dmabufinfo_includedir=$(includedir)/dmabufinfo
dmabufinfo_include_HEADERS := include/dmabufinfo/dmabufinfo.h
dmabufinfo_include_HEADERS += include/dmabufinfo/dmabuf_sysfs_stats.h
# Build tool dmabufinfotest
#bin_PROGRAMS = dmabufinfo_test
#dmabufinfo_test_SOURCES  =    dmabufinfo_test.cpp
#dmabufinfo_test_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
#dmabufinfo_test_CPPFLAGS += -I$(top_srcdir)/include
#dmabufinfo_test_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
#dmabufinfo_test_CPPFLAGS += -std=c++17
#dmabufinfo_test_CPPFLAGS +=  -I$(srcdir)/include
#dmabufinfo_test_CPPFLAGS +=  @LIBBASE_CFLAGS@ @LIBION_CFLAGS@
#dmabufinfo_test_LDFLAGS  =   @LIBBASE_LIBS@  @LIBION_LIBS@ @GTEST_LIBS@ -lion
#dmabufinfo_test_LDADD   =   libdmabufinfo.la

pkgconfigdir := $(libdir)/pkgconfig
pkgconfig_DATA := libdmabufinfo.pc
EXTRA_DIST := $(pkgconfig_DATA)
