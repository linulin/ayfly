INCLUDES = -I$(top_srcdir)/src/libayfly -I$(top_srcdir)/src/libayfly/z80ex -I$(top_srcdir)/src/libayfly/z80ex/include $(all_includes)

bin_PROGRAMS = ayfly_dumper
ayfly_dumper_SOURCES = dumper_main.cpp

if IS_UNIX
EXTRAINCLUDES = $(SDL_CFLAGS)
EXTRALDADD = $(SDL_LIBS)
endif

if IS_WINDOWS
EXTRAINCLUDES = $(DX_CFLAGS)
EXTRALDADD = $(DX_LIBS)
endif

INCLUDES += $(EXTRAINCLUDES)

ayfly_dumper_LDADD = $(top_builddir)/src/libayfly/libayfly.a $(SDL_LIBS) $(DX_LIBS)

datarootdir = @datarootdir@