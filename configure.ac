AC_INIT([camera_test], [0.1], [andre.silva@freescale.com])
AM_INIT_AUTOMAKE([-Wall -Werror foreign])
AC_PROG_CC
AC_CONFIG_HEADERS([config.h])
AC_CHECK_HEADERS([fcntl.h stdint.h stdlib.h string.h sys/ioctl.h unistd.h])

# Checks for library functions.
AC_FUNC_MMAP
AC_CHECK_FUNCS([gettimeofday memset munmap])

##########################################################################
# Checks for programs needed for tests
##########################################################################

AC_CONFIG_FILES([Makefile
		src/Makefile])

AC_OUTPUT
