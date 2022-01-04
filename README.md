# uvaletter

This is an unofficial LaTeX package providing a letterhead template for the University of Amsterdam. The layout is a LaTeX port of the [official template](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/downloadstools/brief/brief.html) and it is entirely compliant with the University's [house style](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/huisstijl.html).

![](https://github.com/piazzai/cvless/blob/master/demo.jpg)

## Installation

The package is not yet hosted on CTAN. To install it, clone the repository and place `uvaletter.sty` file in the directory of your letter document. Then, just write `\usepackage{uvaletter}` in the document preamble, as shown in the image above.

If you plan to use the package for multiple documents, or simply do not want to clutter your directory, you can move `uvaletter.sty` files to `$HOME/texmf/tex/latex`, which is automatically searched by LaTeX. If you do not have such folder yet, you can create one ([read here](https://www.ias.edu/math/computing/faq/local-latex-style-files)).

## Options

The package can be loaded with a `pageno` option, as shown in the demo image, which enables page numbering.
