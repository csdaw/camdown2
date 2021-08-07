camdown
================

## Render a single chapter

1.  Open the **.Rmd** file of a chapter.
2.  Copy the following YAML header which uses the
    **templates/chapter.tex** template, and specifies the desired output
    e.g. `bookdown::pdf_document2`. See below for an example.
3.  Run
    `rmarkdown::render("chapter-name.Rmd", output_format = "bookdown::pdf_document2")`
    in the console. Don’t use the `Knit` button, it will try to render
    the entire thesis.
4.  Be sure to **remove the YAML header when you are done** and want to
    `Knit` the entire thesis again.

``` yaml
---
#########################################
# options for knitting a single chapter #
#########################################
output:
  bookdown::pdf_document2:
    template: templates/chapter.tex
    citation_package: natbib
    pandoc_args: "--top-level-division=chapter"
documentclass: PhDThesisPSnPDF
classoption: a4paper, 12pt, times, numbered, print, index
bibliography: [references/references.bib]
bibliography-heading: References
---
```
