# texmf

This repo stores all the *LaTeX* files that I use for every article/project.
This repo should be particularly useful to reproduce the same **.pdf** outputs without too many migraines when trying to compile from another machine.

It also has the unique **.bib** file that I will keep using and updating here.

I should check that the class (**.cls**) and bibliographic-style (**.bst**) files required by journals are up to date.

The `texmf/` directory and the following tree were manually created (and did not came to life just by installing TexLive). That is, I had to build the tree below (using `mkdir`) and copy/download the files myself from the command-line interface (CLI).

## Tree:
```
texmf
├── bibtex
│   ├── bib
│   │   └── all_my_references_BP.bib
│   └── bst
│       └── agufull08.bst
└── tex
    └── latex
        └── local
            └── agujournal.cls
```

## To Do

- [ ] Test on other machines
- [ ] Test multiple **.bst** files
- [ ] Test multiple **.cls** files

## Notes

The directory tree of a LaTeX article should be like below, and authors should open the manuscript where it is (i.e., `cd` to where **manuscript.tex** is).
Do not have a subdirectory for the manuscript!
This is because when compiling, `epstopdf` only has the right to write in subfolders (e.g., cannot write in `../figures`) and will only be able to convert **.eps** to **.pdf** if the current working directory is parent to the `figures/` directory.
```
.
├── figures
│   ├── ... (pdf converted files)
│   ├── figure_1_for_example-eps-converted-to.pdf
│   └── figure_1_for_example.eps
├── ... (auxiliary files, .pdf, .aux, .log, .etc)
└── manuscript.tex
```

## Cheat Sheet for my vim/skim setup for LaTeX

If all is installed correctly:
- gvim for editor
- skim for viewer
- vimtex plugin for LaTeX stuff

I should be able to do the following:

### Backward search 

In skim, press `CTRL-SHIFT-click` and gvim should point to the corresponding point in the **.tex**.

### Forward search 

In gvim, when in normal mode (not in insert mode) press `,r` and skim should point to the corresponding point in the **.pdf**.

