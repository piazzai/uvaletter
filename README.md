# uvaletter

This is an unofficial LaTeX package that provides a letterhead template for the University of Amsterdam. The layout is a LaTeX port of the [official template](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/downloadstools/brief/brief.html) (in Word) and it is entirely compliant with the University's [house style](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/huisstijl.html).

![](https://github.com/piazzai/uvaletter/blob/master/demo.jpg)

## Installation

The package is not yet hosted on CTAN. To install it, clone the repository and place the file `uvaletter.sty` in the directory of your TeX document. Then, just write `\usepackage{uvaletter}` in the preamble, as shown in the image above.

If you plan to use the package for multiple documents, or simply do not want to clutter your directory, you can move the file `uvaletter.sty` to `$HOME/texmf/tex/latex`, which is automatically searched by LaTeX. If you do not have such folder yet, you can create one ([read here](https://www.ias.edu/math/computing/faq/local-latex-style-files)).

## Usage

The package can be loaded with a `pageno` option that enables page numbering, as shown in the image above. Be aware that in order for the layout to be displayed, your letter body should be wrapped in a `letterhead` environment. Below is a minimal working example:

```tex
\documentclass{letter}
\usepackage{uvaletter}

\recipient{}
\department{}
\visiting{}
\postal{}
\website{}
\date{}
\yourreference{}
\ourreference{}
\contactperson{}
\phone{}
\email{}
\subject{}
\enclosed{}

\begin{document}
\begin{letterhead}

 Hello world!

\end{letterhead}
\end{document}
```

The package requires a file called `logo.jpg` to be placed in your document directory. This repository provides the general logo of the University of Amsterdam, which could be changed to the logo of a specific faculty, department, or institute. All logos of the University can be found [here](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/huisstijlelementen/logo/logo.html).
