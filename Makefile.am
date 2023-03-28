AM_CPPFLAGS := \
    -W \
    -Wall \
    -Wextra \
    -Wunused \
    -Wno-missing-field-initializers

ACLOCAL_AMFLAGS = -I m4


SUBDIRS = libdmabufinfo . tools

# Build libmeminfo.so
libmeminfo_sources = pageacct.cpp procmeminfo.cpp sysmeminfo.cpp
lib_LTLIBRARIES = libmeminfo.la
libmeminfo_la_SOURCES = $(libmeminfo_sources)
libmeminfo_la_CPPFLAGS = -I$(top_srcdir)/include -I$(top_srcdir)/include/meminfo
libmeminfo_la_CPPFLAGS += -I$(top_srcdir)/libdmabufinfo/include
libmeminfo_la_CPPFLAGS += $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
libmeminfo_la_CPPFLAGS += -std=c++17
libmeminfo_la_CPPFLAGS += @LIBBASE_CFLAGS@ 
libmeminfo_la_LDFLAGS = @LIBBASE_LIBS@ -L./libdmabufinfo/ -ldmabufinfo 
# Export headers
libmeminfoinfo_includedir=$(includedir)/meminfo


# Build test libmeminfo_test
bin_PROGRAMS = libmeminfo_test
libmeminfo_test_SOURCES  =    libmeminfo_test.cpp
libmeminfo_test_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
libmeminfo_test_CPPFLAGS += -I$(top_srcdir)/include
libmeminfo_test_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
libmeminfo_test_CPPFLAGS += -std=c++17
libmeminfo_test_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
libmeminfo_test_LDFLAGS  =   @LIBBASE_LIBS@  @GTEST_LIBS@
libmeminfo_test_LDADD   =   libmeminfo.la

install-data-hook:
	$(install_sh_DATA) testdata1/vmallocinfo      $(DESTDIR)$(bindir)/testdata1/vmallocinfo
	$(install_sh_DATA) testdata1/mm_stat          $(DESTDIR)$(bindir)/testdata1/mm_stat
	$(install_sh_DATA) testdata1/smaps            $(DESTDIR)$(bindir)/testdata1/smaps
	$(install_sh_DATA) testdata1/maps_short      $(DESTDIR)$(bindir)/testdata1/maps_short
	$(install_sh_DATA) testdata1/smaps_short      $(DESTDIR)$(bindir)/testdata1/smaps_short
	$(install_sh_DATA) testdata2/mem_used_total   $(DESTDIR)$(bindir)/testdata2/mem_used_total

# Build test ibmeminfo_benchmark
#bin_PROGRAMS += ibmeminfo_benchmark
#ibmeminfo_benchmark_SOURCES  =    libmeminfo_benchmark.cpp
#ibmeminfo_benchmark_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
#ibmeminfo_benchmark_CPPFLAGS += -I$(top_srcdir)/include
#ibmeminfo_benchmark_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
#ibmeminfo_benchmark_CPPFLAGS += -std=c++17
#ibmeminfo_benchmark_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
#ibmeminfo_benchmark_LDFLAGS  =   @LIBBASE_LIBS@ @GTEST_LIBS@
#ibmeminfo_benchmark_LDADD   =   libmeminfo.la

pkgconfigdir := $(libdir)/pkgconfig
pkgconfig_DATA := libmeminfo.pc
EXTRA_DIST := $(pkgconfig_DATA)


