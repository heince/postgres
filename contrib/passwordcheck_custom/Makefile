# contrib/passwordcheck_custom/Makefile

MODULE_big = passwordcheck_custom
OBJS = passwordcheck_custom.o $(WIN32RES)
PGFILEDESC = "passwordcheck_custom - strengthen user password checks"

# uncomment the following two lines to enable cracklib support
# PG_CPPFLAGS = -DUSE_CRACKLIB '-DCRACKLIB_DICTPATH="/usr/lib/cracklib_dict"'
# SHLIB_LINK = -lcrack

REGRESS = passwordcheck_custom

ifdef USE_PGXS
PG_CONFIG = pg_config
PGXS := $(shell $(PG_CONFIG) --pgxs)
include $(PGXS)
else
subdir = contrib/passwordcheck_custom
top_builddir = ../..
include $(top_builddir)/src/Makefile.global
include $(top_srcdir)/contrib/contrib-global.mk
endif
