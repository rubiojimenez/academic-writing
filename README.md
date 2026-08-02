# Writing Toolkit

Curated collection of LaTeX templates and document-building utilities for **streamlining writing**.

I wrote these tools for my own use and I refine them as I go. 
Some are still tailored to my personal workflow, but should be straightforward to adapt.

The repository also includes my VSCodium setup, which I use for Python, HTML, CSS, and occasionally LaTeX and Markdown. 

For focused writing I prefer Texmaker, while collaborative projects tend to end up on Overleaf.
For Markdown and other plain text files I prefer Kate.
I sometimes brainstorm in Writer because it feels more like working on paper.
I have no automation for these additional workflows, and they are therefore not represented here.

At present, the repository focuses on scientific writing, though I expect it to evolve into a more general writing toolkit over time.

## A modular writing architecture

For my LaTeX documents, I have adopted a modular preamble separating packages, configuration and macros:

```text
preamble/
├── config.tex
├── macros.tex
└── packages.tex
```

This makes templates easier to use and maintain. 

I am gradually migrating older templates to this structure.


## Templates

The document types covered are

- journal articles;
- referee responses;
- conference abstracts;
- abstract collections;
- research proposals; and
- cover letters.

For each document, both

```text
main.tex
main.pdf
```

are provided to allow a quick preview of the final output.

I use the Libertinus typeface together with the corresponding Libertinus math fonts. 
Besides liking its appearance, it is open source, widely available, and produces consistent output across Linux, macOS and Windows.


## Command-line utilities

Helper scripts are also provided for automating repetitive tasks:

`builddown`: Converts Markdown documents into PDF using Pandoc and XeLaTeX.

`buildtex`: A wrapper around the standard LaTeX toolchain supporting

- PDF compilation with BibTeX, including bibunits;
- generation of files for arXiv submission;
- project cleanup; and
- standard compilation while retaining intermediate files.

`gitush`: A wrapper around

```bash
git add .
git commit -m "<message>"
git push
```

It is intended for the case where everything is ready to go.

`sortbib`: Sorts BibTeX databases alphabetically by entry key and orders the fields likewise within each entry.

I use this less nowadays in favour of JabRef, but it is still useful when handling BibTeX files directly.

`startop`: Launches my preferred working environment. 

My workflow is essentially filesystem-first, so I usually work from Dolphin, using its integrated terminal and launching external editors as needed.

## Requirements

Depending on which templates and utilities you use, you may need

- TeX Live;
- XeLaTeX;
- Pandoc;
- Python 3 with the required modules;
- Git.

Additionally,

- `startop` uses Dolphin and VSCodium.

## Contributing

Both suggestions and contributions of additional templates are welcome.

## License

This project is licensed under the GPL-3.0 License.
