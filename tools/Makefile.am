AM_CPPFLAGS := \
    -W \
    -Wall \
    -Wextra \
    -Wunused \
    -Wno-missing-field-initializers

ACLOCAL_AMFLAGS = -I m4


# Build librank
bin_PROGRAMS = librank
librank_SOURCES  =    librank.cpp
librank_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
librank_CPPFLAGS += -I$(top_srcdir)/include
librank_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
#librank_CPPFLAGS += -std=c++17
librank_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
librank_LDFLAGS  =   @LIBBASE_LIBS@ @GTEST_LIBS@
librank_LDADD   =   ../libmeminfo.la

# Build procmem
bin_PROGRAMS += procmem
procmem_SOURCES  =    procmem.cpp
procmem_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
procmem_CPPFLAGS += -I$(top_srcdir)/include
procmem_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
procmem_CPPFLAGS += -std=c++17
procmem_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
procmem_LDFLAGS  =   @LIBBASE_LIBS@ @GTEST_LIBS@
procmem_LDADD   =   ../libmeminfo.la

# Build procrank
bin_PROGRAMS += procrank
procrank_SOURCES  =    procrank.cpp
procrank_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
procrank_CPPFLAGS += -I$(top_srcdir)/include
procrank_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
procrank_CPPFLAGS += -std=c++17
procrank_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
procrank_LDFLAGS  =   @LIBBASE_LIBS@ @GTEST_LIBS@
procrank_LDADD   =   ../libmeminfo.la

# Build showmap
bin_PROGRAMS += showmap
showmap_SOURCES  =    showmap.cpp
showmap_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
showmap_CPPFLAGS += -I$(top_srcdir)/include
showmap_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
showmap_CPPFLAGS += -std=c++17
showmap_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
showmap_LDFLAGS  =   @LIBBASE_LIBS@ @GTEST_LIBS@
showmap_LDADD   =   ../libmeminfo.la

#Build wsstop
bin_PROGRAMS += wsstop
wsstop_SOURCES  =    wsstop.cpp
wsstop_CPPFLAGS =   $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
wsstop_CPPFLAGS += -I$(top_srcdir)/include
wsstop_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
wsstop_CPPFLAGS += -std=c++17
wsstop_CPPFLAGS +=  @LIBBASE_CFLAGS@ 
wsstop_LDFLAGS  =   @LIBBASE_LIBS@ @GTEST_LIBS@
wsstop_LDADD   =   ../libmeminfo.la
