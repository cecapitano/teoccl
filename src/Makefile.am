## Process this file with automake to produce Makefile.in
#

ACLOCAL_AMFLAGS = -I m4

AM_CPPFLAGS = \
	-DPACKAGE_LOCALE_DIR=\""$(prefix)/$(DATADIRNAME)/locale"\" \
	-DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
	-DPACKAGE_DATA_DIR=\""$(datadir)"\" $(TEOCCL_CFLAGS)

AM_CFLAGS = \
	-g -Wall \
	-std=gnu11 \
	-fno-strict-aliasing \
	-fPIC \
	-I../include \
	-Wpointer-arith

AM_CXX = clang++
AM_CXXFLAGS = \
	-g -Wall \
	-std=c++14 \
	-fPIC \
	-I../include

## Debug info
if DEBUG
  AM_CFLAGS += -g3 -O0
  AM_CXXFLAGS += -g3 -O0
else
  AM_CFLAGS += -O2
  AM_CXXFLAGS += -O2
endif

AM_LDFLAGS = 

LIBS =

lib_LTLIBRARIES = libteoccl.la


libteoccl_la_SOURCES = \
	teoccl/memory.c \
	teoccl/queue.c \
	teoccl/hash.c \
	teoccl/map.c \
	teoccl/list.c \
	teoccl/array_list.c \
	teoccl/linked_list.c \
	teoccl/deque.c \
	teoccl/que.c \
	teoccl/stack.c

libteocclincludedir=$(includedir)/libteoccl

nobase_libteocclinclude_HEADERS = \
	../include/teoccl/memory.h \
	../include/teoccl/list.h \
	../include/teoccl/hash.h \
	../include/teoccl/array_list.h \
	../include/teoccl/linked_list.h \
	../include/teoccl/map.h \
	../include/teoccl/map.hpp \
	../include/teoccl/queue.h \
	../include/teoccl/queue.hpp \
	../include/teoccl/deque.h \
	../include/teoccl/que.h \
	../include/teoccl/stack.h \
	teoccl/teoccl.hpp

libteoccl_la_LDFLAGS = $(AM_LDFLAGS) -version-info $(LIBRARY_CURRENT):$(LIBRARY_REVISION):$(LIBRARY_AGE)

libteoccl_la_LIBADD = $(TEOCCL_LIBS)
