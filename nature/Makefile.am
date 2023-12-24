backgrounddir = $(datadir)/backgrounds/cafe/nature

background_DATA =\
	Aqua.jpg \
	Blinds.jpg \
	Dune.jpg \
	FreshFlower.jpg \
	Garden.jpg \
	GreenMeadow.jpg \
	LadyBird.jpg \
	RainDrops.jpg \
	Storm.jpg \
	TwoWings.jpg \
	Wood.jpg \
	YellowFlower.jpg

metadata_in_files = cafe-nature.xml.in
metadatadir = $(datadir)/cafe-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)

$(metadata_DATA): $(metadata_in_files)
	$(AM_V_GEN) GETTEXTDATADIR=$(top_srcdir) $(MSGFMT) --xml --template $< -d $(top_srcdir)/po -o $@

noinst_DATA = cafe-nature.xml.in
CLEANFILES = cafe-nature.xml cafe-nature.xml.in

EXTRA_DIST = \
	$(background_DATA) \
	cafe-nature.xml.in.in \
	meson.build

cafe-nature.xml.in: cafe-nature.xml.in.in Makefile
	$(AM_V_GEN)sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/cafe-nature.xml.in.in > cafe-nature.xml.in.tmp \
	&& mv cafe-nature.xml.in.tmp cafe-nature.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk
