# Working on the book

Read the first few chapters of the [Bookdown book](https://bookdown.org/yihui/bookdown/) unless 
you already know Bookdown.

Use 100 characters as text width in files (in vi/vim: `:set tw=100`; there is a modeline in each file).

SVG figures in `img/` need to be converted to png. This can either be done by opening every file in
e.g. Inkscape or running the following command in the `img` directory (which assumes you have
Inkscape installed):

```
make all_pngs
```

The book can be built from inside RStudio by clicking "Build website" or "Build Book" in the "Build" 
pane in the upper right of RStudio.
