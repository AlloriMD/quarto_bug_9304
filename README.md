# Demonstration of figure cross-referencing bug in a Quarto Book project

This sample Quarto Book is intended to demonstrate a bug ([issue 9304](https://github.com/quarto-dev/quarto-cli/issues/9304)) that affects figure cross-referencing. Specifically, when book sections are stored in a subdirectory and are listed in `_quarto.yml` using the format `./_chapters/ch01.qmd`, then crossrefs to the figure are not resolved to "Figure 1" but instead remain listed as "fig-id". When the book sections are listed in `_quarto.yml` in the format `_chapters/ch01.qmd`  (note the missing `./` prefix), then the crossrefs appear properly as "Figure 1".

In the first chapter of this sample book, several figures are included, using different means of figure specification: simple Markdown notation; Markdown notation within a DIV; simple computational plot within a code chunk; and a computational plot within a code chunk that is within a DIV. The `./` bug affects each type of figure; and removing the `./` in `_quarto.yml` corrects the bug for each figure type.

There is a .gif screen capture that demonstrates the problem in action.
