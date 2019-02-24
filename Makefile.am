SUBDIRS = src

AUTOMAKE_OPTIONS = foreign
 
RPMBUILD = rpmbuild
rpm: dist
	$(RPMBUILD) -ta $(distdir).tar.gz

desktopdir = $(datadir)/applications
desktop_DATA = barrage.desktop

EXTRA_DIST = BUGS README COPYING AUTHORS ChangeLog INSTALL NEWS TODO \
	$(PACKAGE).spec $(PACKAGE).spec.in barrage.desktop \
	barrage16.png barrage32.png barrage48.png

install-data-local:
	$(mkinstalldirs) $(DESTDIR)$(datadir)/icons/hicolor/16x16/apps
	$(mkinstalldirs) $(DESTDIR)$(datadir)/icons/hicolor/32x32/apps
	$(mkinstalldirs) $(DESTDIR)$(datadir)/icons/hicolor/48x48/apps
	$(INSTALL_DATA) barrage16.png $(DESTDIR)$(datadir)/icons/hicolor/16x16/apps/barrage.png
	$(INSTALL_DATA) barrage32.png $(DESTDIR)$(datadir)/icons/hicolor/32x32/apps/barrage.png
	$(INSTALL_DATA) barrage48.png $(DESTDIR)$(datadir)/icons/hicolor/48x48/apps/barrage.png

uninstall-local:
	rm -f $(DESTDIR)$(datadir)/icons/hicolor/16x16/apps/barrage.png
	rm -f $(DESTDIR)$(datadir)/icons/hicolor/32x32/apps/barrage.png
	rm -f $(DESTDIR)$(datadir)/icons/hicolor/48x48/apps/barrage.png

	
