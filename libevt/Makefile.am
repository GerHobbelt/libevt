AM_CPPFLAGS = \
	-DLOCALEDIR=\"$(datadir)/locale\" \
	-I../include -I$(top_srcdir)/include \
	-I../common -I$(top_srcdir)/common \
	@LIBCERROR_CPPFLAGS@ \
	@LIBCTHREADS_CPPFLAGS@ \
	@LIBCDATA_CPPFLAGS@ \
	@LIBCLOCALE_CPPFLAGS@ \
	@LIBCNOTIFY_CPPFLAGS@ \
	@LIBCSPLIT_CPPFLAGS@ \
	@LIBUNA_CPPFLAGS@ \
	@LIBCFILE_CPPFLAGS@ \
	@LIBCPATH_CPPFLAGS@ \
	@LIBBFIO_CPPFLAGS@ \
	@LIBFCACHE_CPPFLAGS@ \
	@LIBFDATA_CPPFLAGS@ \
	@LIBFDATETIME_CPPFLAGS@ \
	@LIBFGUID_CPPFLAGS@ \
	@LIBFWNT_CPPFLAGS@ \
	@PTHREAD_CPPFLAGS@ \
	@LIBEVT_DLL_EXPORT@

lib_LTLIBRARIES = libevt.la

libevt_la_SOURCES = \
	evt_end_of_file_record.h \
	evt_event_record.h \
	evt_file_header.h \
	evt_record.h \
	libevt.c \
	libevt_codepage.h \
	libevt_debug.c libevt_debug.h \
	libevt_definitions.h \
	libevt_end_of_file_record.c libevt_end_of_file_record.h \
	libevt_event_record.c libevt_event_record.h \
	libevt_error.c libevt_error.h \
	libevt_extern.h \
	libevt_file.c libevt_file.h \
	libevt_file_header.c libevt_file_header.h \
	libevt_io_handle.c libevt_io_handle.h \
	libevt_libbfio.h \
	libevt_libcdata.h \
	libevt_libcerror.h \
	libevt_libclocale.h \
	libevt_libcnotify.h \
	libevt_libcthreads.h \
	libevt_libfcache.h \
	libevt_libfdata.h \
	libevt_libfdatetime.h \
	libevt_libfwnt.h \
	libevt_libuna.h \
	libevt_notify.c libevt_notify.h \
	libevt_record.c libevt_record.h \
	libevt_record_values.c libevt_record_values.h \
	libevt_strings_array.c libevt_strings_array.h \
	libevt_support.c libevt_support.h \
	libevt_types.h \
	libevt_unused.h

libevt_la_LIBADD = \
	@LIBCERROR_LIBADD@ \
	@LIBCTHREADS_LIBADD@ \
	@LIBCDATA_LIBADD@ \
	@LIBCLOCALE_LIBADD@ \
	@LIBCNOTIFY_LIBADD@ \
	@LIBCSPLIT_LIBADD@ \
	@LIBUNA_LIBADD@ \
	@LIBCFILE_LIBADD@ \
	@LIBCPATH_LIBADD@ \
	@LIBBFIO_LIBADD@ \
	@LIBFCACHE_LIBADD@ \
	@LIBFDATA_LIBADD@ \
	@LIBFDATETIME_LIBADD@ \
	@LIBFGUID_LIBADD@ \
	@LIBFWNT_LIBADD@ \
	@PTHREAD_LIBADD@

libevt_la_LDFLAGS = -no-undefined -version-info 1:0:0

EXTRA_DIST = \
	libevt_definitions.h.in \
	libevt.rc \
	libevt.rc.in

DISTCLEANFILES = \
	libevt_definitions.h \
	libevt.rc \
	Makefile \
	Makefile.in

sources-local: $(BUILT_SOURCES)

splint-local:
	@echo "Running splint on libevt ..."
	-splint -preproc -redef $(DEFS) $(DEFAULT_INCLUDES) $(INCLUDES) $(AM_CPPFLAGS) $(libevt_la_SOURCES)

