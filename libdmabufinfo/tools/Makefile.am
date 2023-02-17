AM_CPPFLAGS := \
    -W \
    -Wall \
    -Wextra \
    -Wunused \
    -Wno-missing-field-initializers

ACLOCAL_AMFLAGS = -I m4

# Build tool dmabuf_dump
bin_PROGRAMS = dmabuf_dump

dmabuf_dump_SOURCES = dmabuf_dump.cpp
dmabuf_dump_CPPFLAGS = $(AM_CPPFLAGS) -Wno-error=pointer-to-int-cast
dmabuf_dump_CPPFLAGS += -I$(top_srcdir)/include
dmabuf_dump_CPPFLAGS += -std=c++17
dmabuf_dump_CPPFLAGS += @LIBBASE_CFLAGS@ 
dmabuf_dump_CPPFLAGS += -I$(srcdir)/../include
dmabuf_dump_LDFLAGS = @LIBBASE_LIBS@ @LIBION_LIBS@ -lion
dmabuf_dump_LDADD   = ../libdmabufinfo.la

