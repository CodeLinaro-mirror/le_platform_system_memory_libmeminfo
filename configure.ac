AC_PREREQ(2.61)
AC_INIT([libmeminfo],1.0.0)
AM_INIT_AUTOMAKE([-Wall gnu foreign])
AC_CONFIG_SRCDIR([Makefile.am])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])

# Check for programs
AM_PROG_AS
AC_PROG_CC
AM_PROG_CC_C_O
AC_PROG_LIBTOOL
AC_PROG_AWK
AC_PROG_CPP
AC_PROG_CXX
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
PKG_PROG_PKG_CONFIG

PKG_CHECK_MODULES([LIBBASE], [libbase])
AC_SUBST([LIBBASE_CFLAGS])
AC_SUBST([LIBBASE_LIBS])

PKG_CHECK_MODULES([LIBBASE], [libion])
AC_SUBST([LIBION_CFLAGS])
AC_SUBST([LIBION_LIBS])

PKG_CHECK_MODULES([GTEST], [gtest])
AC_SUBST([GTEST_CFLAGS])
AC_SUBST([GTEST_LIBS])

AC_ARG_WITH(sanitized-headers,
        AS_HELP_STRING([--with-sanitized-headers=DIR],
                [Specify the location of the sanitized Linux headers]),
        [CPPFLAGS="$CPPFLAGS -I $withval"])

AC_CONFIG_FILES([ \
    libdmabufinfo/Makefile \
    libdmabufinfo/tools/Makefile \
    libdmabufinfo/libdmabufinfo.pc \
    Makefile \
    libmeminfo.pc \
    tools/Makefile \
])
AC_CONFIG_LINKS(testdata1/vmallocinfo:testdata1/vmallocinfo)
AC_CONFIG_LINKS(testdata1/mm_stat:testdata1/mm_stat)
AC_CONFIG_LINKS(testdata1/smaps:testdata1/smaps)
AC_CONFIG_LINKS(testdata1/maps_short:testdata1/maps_short)
AC_CONFIG_LINKS(testdata1/smaps_short:testdata1/smaps_short)
AC_CONFIG_LINKS(testdata2/mem_used_total:testdata2/mem_used_total)
AC_OUTPUT

