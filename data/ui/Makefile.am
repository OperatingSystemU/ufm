NULL=

# GtkBuilder UI definition files
uidir=$(datadir)/pcmanfm/ui
ui_SOURCES = \
	pref.glade \
	desktop-pref.glade \
	autorun.glade \
	$(NULL)
ui_in_files= \
	$(ui_SOURCES) \
	about.glade \
	$(NULL)
ui_DATA = $(ui_in_files:.glade=.ui)

EXTRA_DIST = \
	$(ui_SOURCES) \
	$(ui_DATA) \
	$(NULL)

# Purge GtkBuilder UI files
.glade.ui:
	sed 's/<!--.*-->//' < $< | sed ':a;N;$$!ba;s/ *\n *</</g' > $@
