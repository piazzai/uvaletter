<!--
uvaletter v1.0.0
author: Michele Piazzai
contact: michele.piazzai@uc3m.es
license: MIT
-->

# uvaletter

This is an unofficial LaTeX package that provides a letterhead template for the University of Amsterdam. The layout is a LaTeX port of the [official Word template](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/downloadstools/brief/brief.html) of the University, and it is entirely compliant with the University's [house style](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/huisstijl.html).

![](https://github.com/piazzai/uvaletter/blob/master/demo/demo.jpg)

## Installation

The package is hosted on CTAN and distributed as part of MikTex and TeXLive. It can also be installed manually by cloning this repository in your `$HOME/texmf/tex/latex` folder. This is useful if you wish to change the logo. If you do not have this folder already, you can [create it](https://www.ias.edu/math/computing/faq/local-latex-style-files).

## Usage

The package can be loaded with a `pageno` option that enables page numbering. Be aware that, in order for the layout to display, your letter body should be wrapped in a `letterhead` environment.

Here is a minimal working example:

```tex
\documentclass{letter}
\usepackage{uvaletter}

\recipient{foo}
\department{bar}
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

A file called `logo.jpg` is required to be in your document directory. This repository provides the generic logo of the University of Amsterdam, but this can be changed to the logo of a specific faculty, department, or institute. All the official logos of the University can be found [here](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/huisstijlelementen/logo/logo.html).
