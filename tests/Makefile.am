ACLOCAL_AMFLAGS = -I m4

AM_CPPFLAGS = \
	-DPACKAGE_LOCALE_DIR=\""$(prefix)/$(DATADIRNAME)/locale"\" \
	-DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
	-DPACKAGE_DATA_DIR=\""$(datadir)"\" $(TRUDP_CFLAGS)

AM_CFLAGS = \
	-g -Wall \
	-std=gnu11 \
	-I../include

AM_CXX = clang++
AM_CXXFLAGS = \
	-g -Wall \
	-std=c++14 \
	-I../include \
	-std=c++14

## Debug info
if DEBUG
  AM_CFLAGS += -g3 -O0
  AM_CXXFLAGS += -g3 -O0
else
  AM_CFLAGS += -O2
  AM_CXXFLAGS += -O2
endif

AM_LDFLAGS = -L../src/.libs 

LIBS = ../src/.libs/libteoccl.a -lcunit -lCppUTest

noinst_PROGRAMS = teoccl_tst teoccl_cpp_tst

teoccl_tst_SOURCES = main_t.c queue_t.c map_t.c array_list_t.c deque_t.c que_t.c stack_t.c linked_list_t.c CMakeLists.txt
teoccl_cpp_tst_SOURCES = main_cpp_t.cpp queue_cpp_t.cpp map_cpp_t.cpp

testsdir = $(datarootdir)/doc/@PACKAGE@/tests
tests_DATA = $(teoccl_tst_SOURCES) $(teoccl_cpp_tst_SOURCES)

# Remove doc directory on uninstall
uninstall-local:
	-rm -r $(datarootdir)/doc/@PACKAGE@/tests
