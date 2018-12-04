all_pngs: $(subst .svg,.png,$(wildcard *.svg))

%.png: %.svg
	inkscape --export-png $@ $<
