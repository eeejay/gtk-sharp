lib_LTLIBRARIES = $(TARGET)

if ENABLE_GLADE
TARGET = libgladesharpglue-3.la
else
TARGET = 
endif

libgladesharpglue_3_la_LDFLAGS = -module -avoid-version -no-undefined

libgladesharpglue_3_la_SOURCES = 	\
	gladexml.c

nodist_libgladesharpglue_3_la_SOURCES = generated.c

libgladesharpglue_3_la_LIBADD = $(GLADE_LIBS)

INCLUDES = $(GLADE_CFLAGS) $(GTK_SHARP_VERSION_CFLAGS) -I$(top_srcdir)

libgladesharpglue.dll: $(libgladesharpglue_3_la_OBJECTS) libgladesharpglue.rc libgladesharpglue.def
	./build-dll libgladesharpglue-3 $(VERSION)

CLEANFILES = lib*.a lib*.dll

EXTRA_DIST = win32dll.c
