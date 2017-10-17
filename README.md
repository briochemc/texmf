# texmf

This repo stores all the *LaTeX* files that I use for every article/project.
This repo should be particularly useful to reproduce the same **.pdf** outputs without too many migraines when trying to compile from another machine.

It also has the unique **.bib** file that I will keep using and updating here.

I should check that the class (**.cls**) and bibliographic-style (**.bst**) files required by journals are up to date.

The `texmf/` directory and the following tree where not created by installing TexLive: Instead, I had to manually create (`mkdir`) the tree and copy/download the files myself.

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
