cmake_minimum_required(VERSION 2.8.11)

set(VERSION "\"1.7.0\"")
string(TIMESTAMP BUILD_DATE "\"%Y-%m-%d\"")
INCLUDE (CheckIncludeFiles)
configure_file(${CMAKE_CURRENT_SOURCE_DIR}/config.h.cmake ${CMAKE_CURRENT_BINARY_DIR}/config.h)

add_subdirectory(src)


########### install files ###############

#install(FILES  necpp.pc DESTINATION )



#original Makefile.am contents follow:

## not a GNU package. You can remove this line, if
## have all needed files, that a GNU package needs
#
#AUTOMAKE_OPTIONS = foreign 1.4
#ACLOCAL_AMFLAGS = -I m4
#SUBDIRS = src
#
#EXTRA_DIST = \
#	example \
#	html \
#	win32
#
#pkgconfigdir = $(libdir)/pkgconfig
#pkgconfig_DATA = necpp.pc
#
#dist-hook:
#	rm -rf `find $(distdir)testharness/data -name *.out*`
#	rm -rf `find $(distdir)testharness/data -name *.diff*`
