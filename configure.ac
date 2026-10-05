#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.59])
AC_INIT([tsar],[2.2.0],[https://github.com/mingzym/tsar])
#AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE([-Wall -Werror foreign 1.9.0])

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL

# Checks for libraries.
# FIXME: Replace `main' with a function in `-ldl':
AC_CHECK_LIB([dl], [main])

# Checks for header files.
AC_SUBST([prefix])
AC_SUBST([exec_prefix])
AC_SUBST([libdir])

AC_CONFIG_SRCDIR([include/output_print.h])
# Checks for library functions.

AC_CONFIG_FILES([rpm/tsar.spec])
AC_CONFIG_FILES([Makefile
	        include/define.h
		src/modules/Makefile
		devel/Makefile
		conf/Makefile
		src/Makefile])
AC_OUTPUT
