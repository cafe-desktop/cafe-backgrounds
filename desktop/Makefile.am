backgrounddir = $(datadir)/backgrounds/cafe/desktop

background_DATA = \
	Float-into-MATE.png \
	GreenTraditional.jpg \
	Stripes.png \
	MATE-Stripes-Dark.png \
	MATE-Stripes-Light.png \
	Ubuntu-Cafe-Cold-no-logo.png \
	Ubuntu-Cafe-Dark-no-logo.png \
	Ubuntu-Cafe-Radioactive-no-logo.png \
	Ubuntu-Cafe-Warm-no-logo.png

metadata_in_files = cafe-desktop.xml.in
metadatadir = $(datadir)/cafe-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)

$(metadata_DATA): $(metadata_in_files)
	$(AM_V_GEN) GETTEXTDATADIR=$(top_srcdir) $(MSGFMT) --xml --template $< -d $(top_srcdir)/po -o $@

noinst_DATA = cafe-desktop.xml.in
CLEANFILES = cafe-desktop.xml cafe-desktop.xml.in

EXTRA_DIST = \
	$(background_DATA) \
	cafe-desktop.xml.in.in \
	meson.build

cafe-desktop.xml.in: cafe-desktop.xml.in.in Makefile
	$(AM_V_GEN)sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/cafe-desktop.xml.in.in > cafe-desktop.xml.in.tmp \
	&& mv cafe-desktop.xml.in.tmp cafe-desktop.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk
