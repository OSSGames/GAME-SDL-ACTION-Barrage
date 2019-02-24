DEFS = @DEFS@ @src_dir_flag@ @audio_flag@

bin_PROGRAMS = barrage

barrage_SOURCES = \
	main.c\
	particle.c\
	shots.c\
	units.c\
	data.c\
	chart.c\
	bfield.c\
	menu.c\
	SFont.c

barrage_LDFLAGS = 
barrage_LDADD = @audio_lib@ -lm

EXTRA_DIST = \
	defs.h particle.h shots.h units.h\
	data.h bfield.h menu.h SFont.h chart.h

SUBDIRS = gfx sounds

uninstall-local:
	rm -rf $(DESTDIR)$(src_dir)

