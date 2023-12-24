backgrounddir = $(datadir)/backgrounds/cafe/abstract

background_DATA = \
	Arc-Colors-Transparent-Wallpaper.png \
	Flow.png \
	Gulp.png \
	Silk.png \
	Spring.png \
	Waves.png \
	Elephants.jpg \
	Elephants_3840x2160.jpg \
	Elephants_5640x3172.jpg

metadata_in_files = cafe-abstract.xml.in
metadatadir = $(datadir)/cafe-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)

$(metadata_DATA): $(metadata_in_files)
	$(AM_V_GEN) GETTEXTDATADIR=$(top_srcdir) $(MSGFMT) --xml --template $< -d $(top_srcdir)/po -o $@

noinst_DATA = cafe-abstract.xml.in
CLEANFILES = cafe-abstract.xml cafe-abstract.xml.in

EXTRA_DIST = \
	$(background_DATA) \
	cafe-abstract.xml.in.in \
	meson.build

cafe-abstract.xml.in: cafe-abstract.xml.in.in Makefile
	$(AM_V_GEN)sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/cafe-abstract.xml.in.in > cafe-abstract.xml.in.tmp \
	&& mv cafe-abstract.xml.in.tmp cafe-abstract.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk
