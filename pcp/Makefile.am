AM_CPPFLAGS = -D_GNU_SOURCE -I .. -I @PGSQL_INCLUDE_DIR@

lib_LTLIBRARIES = libpcp.la
libpcp_la_SOURCES = pcp.h ../pool_type.h md5.h pcp.c pcp_stream.h pcp_stream.c pcp_error.c md5.c strlcpy.c
libpcp_la_LIBS =
include_HEADERS = pcp.h libpcp_ext.h ../pool_type.h ../pool_process_reporting.h

md5.c: ../md5.c
	rm -f $@ && ln -s $< .
md5.h: ../md5.h
	rm -f $@ && ln -s $< .

bin_PROGRAMS =  pcp_stop_pgpool pcp_node_count pcp_node_info pcp_proc_count pcp_proc_info \
		pcp_systemdb_info pcp_detach_node pcp_attach_node pcp_recovery_node pcp_promote_node \
		pcp_pool_status pcp_watchdog_info
pcp_stop_pgpool_SOURCES = pcp_stop_pgpool.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_stop_pgpool_LDADD = libpcp.la
pcp_stop_pgpool_LDFLAGS =
pcp_node_count_SOURCES = pcp_node_count.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_node_count_LDADD = libpcp.la
pcp_node_info_SOURCES = pcp_node_info.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_node_info_LDADD = libpcp.la
pcp_proc_count_SOURCES = pcp_proc_count.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_proc_count_LDADD = libpcp.la
pcp_proc_info_SOURCES = pcp_proc_info.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_proc_info_LDADD = libpcp.la
pcp_systemdb_info_SOURCES = pcp_systemdb_info.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_systemdb_info_LDADD = libpcp.la
pcp_detach_node_SOURCES = pcp_detach_node.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_detach_node_LDADD = libpcp.la
pcp_attach_node_SOURCES = pcp_attach_node.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_attach_node_LDADD = libpcp.la
pcp_recovery_node_SOURCES = pcp_recovery_node.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_recovery_node_LDADD = libpcp.la
pcp_pool_status_SOURCES = pcp_pool_status.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_pool_status_LDADD = libpcp.la
pcp_promote_node_SOURCES = pcp_promote_node.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_promote_node_LDADD = libpcp.la
pcp_watchdog_info_SOURCES = pcp_watchdog_info.c pcp.h ../getopt_long.c ../getopt_long.h
pcp_watchdog_info_LDADD = libpcp.la
