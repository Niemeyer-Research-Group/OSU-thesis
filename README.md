# OSU thesis

This repo holds a template for Oregon State University graduate theses written
using LaTeX. (NRG members should only be using LaTeX.) This may be helpful for
others at Oregon State for writing theses as well; it should satisfy
[Oregon State University Graduate School requirements](https://gradschool.oregonstate.edu/progress/thesis-guide).
Please let us know if it does not! A copy of the latest formatting guide is in the `beavtex` directory.

The main document is `thesis.tex`, and individual representative chapters are in separate
`*.tex` files. Feel free to keep or change these as appropriate for you, or add new files.
Note that they are currently set up to be included using the `subfiles` package, which
makes it easier to work and compile on a particular chapter at a time by itself.
The `thesis-header.tex` file contains most of the preamble and LaTeX packages, and
you should not need to edit it unless you want to customize the thesis format.

If you have a manuscript-style thesis, see the instructions below.

Initial items to check/change in `thesis.tex`:

 - Replace the placeholders `YOUR NAME` and `THESIS TITLE`
 - Check the degree type specified by `\degree{}`, and change to "Master of Science" if you are pursuing an MS.
 - Update the `\submitdate{}` and `\commencementyear{}` fields.
 - If you aren't an NRG member, you may need to update the `\department{}`, `\major{}`, and `\advisor{}` fields.
 - Put your abstract in the `\abstract{}` environment.
 - Add your acknowledgements.
 - You can include a short dedication line using the `\dedication{}` command; remove if not used.
 - You can include a quote as a preface, if you want, based on the example using the `\epigraph{}` command. Otherwise remove this section.

Beyond that, add content to the existing chapter or replace with other chapters as appropriate for you.
The `%!TEX root = thesis.tex` bit at the top of the files tells most LaTeX editors to automatically
compile the main document, even when you are working on an individual subfile.

The references are contained in `refs.bib`, though this can be replaced with a different file by
changing the `\addbibresource{}` command in `thesis-header.tex`. You can also use multiple BibTeX
files by adding additional `\addbibresource{}` commands. Note that `biber` and `biblatex` are
used to process references in this template, rather than the older `bibtex`.

In the chapters, you can include a quotation that appears right before the chapter title using
the `\epigraphhead{}` command, following the example in the Introduction chapter.

Lastly, the `\graphicspath{}` command in `thesis.tex` specifies a `figures` directory
for all figures, telling LaTeX to look there when you include an image.

## Instructions for manuscript theses/dissertations

Frequently students follow the manuscript thesis format, where their thesis or dissertation is
made up of multiple individually complete manuscripts. This is perfectly fine (and actually what
we typically recommend, particularly for PhD students), but the Graduate School requests the following format:

1. Pretext pages
2. Chapter 1: Overall Introduction
3. Chapter 2: First Manuscript
4. Chapter 3: Second Manuscript
5. Chapter 4+: Additional Manuscripts
6. Chapter n: Overall Conclusions
7. References (manuscripts may have their own reference sections too)
8. Appendices, if applicable

Also, each manuscript chapter must be preceded by a title page with some information about
the manuscript. See the example `manuscript1.tex` file for an example of how to structure these
chapters.

## Acknowledgements

This thesis template uses the `beavtex.cls` class; though the provenance of this document
isn't totally clear, its authors include Neville Mehta, Deling Ren, and John Metta.
