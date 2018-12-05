# Working on the book

Read the first few chapters of the [Bookdown book](https://bookdown.org/yihui/bookdown/) unless 
you already know Bookdown.

Use 100 characters as text width in files (in vi/vim: `:set tw=100`; there is a modeline in each file, 
requires that `set modline` is set(!)).

## Figures

SVG figures in `img/` need to be converted to png. This can either be done by opening every file in
e.g. Inkscape or running the following command in the `img` directory (which assumes you have
Inkscape installed):

```
make all_pngs
```

## Citations

Literature references belong in the `eemis-compbio.bib` file, which is a BibTex copy of a Zotero
group with the same name. Contact Daniel Lundin if you want access.

If you add something to the Zotero group, you need to export it to BibTex with the name
`eemis-compbio.bib` and place it in this directory.

Refering to literature is done like this: `@garrels_bash_2008` (get the name from the bib file).

## Building the book

The book can be built from inside RStudio by clicking "Build Book" in the "Build" pane in the upper
right of RStudio.
