# Working on the book

Read the first few chapters of the [Bookdown book](https://bookdown.org/yihui/bookdown/) unless 
you already know Bookdown.

Use 100 characters as text width in files (in vi/vim: `:set tw=100`; there is a modeline in each file, 
requires that `set modline` is set(!)).

## Conventions

I have used standard capitalization and standard font for program names, i.e. writing "Bash" instead
of e.g. "bash" or `bash`. There are probably remnants of writing in code style, i.e. `bash`, in some
places. Please change if you see them.

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

## Index

You should add index terms to the text: `\index{GUI}GUI`. Try to use basic forms of words, like
nominative for nouns and infinitive for verbs. Also look at what is already used as index terms,
either by grepping for `\index` (`grep -o "\index{[^}]*}" *.Rmd`) or by building the book in PDF
format (HTML does not produce an index).

*Note:* Latex is sensitive to underscore characters. In most cases it works fine to have words with
underscores in the text, but *not in index terms*. To create an index term for e.g. `.bash_profile`
you have to escape the underscore: `\index{.bash_profile}`.

## Building the book

The book can be built from inside RStudio by clicking "Build Book" in the "Build" pane in the upper
right of RStudio.
