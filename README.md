<!--
uvaletter v1.0.0
author: Michele Piazzai
contact: michele.piazzai@uc3m.es
license: MIT
-->

# uvaletter

This is an unofficial LaTeX package that provides a letterhead template for the University of Amsterdam. The layout mimics the [official Word template](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/downloadstools/brief/brief.html) of the University, and it is entirely compliant with the University's [house style](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/huisstijl.html).

![](https://github.com/piazzai/uvaletter/blob/master/demo/demo.jpg)

## Installation

This package is hosted on CTAN and distributed as part of MikTex and TeXLive. It can also be installed manually by cloning this repository in your `$HOME/texmf/tex/latex` folder. If you do not have such a folder, you can [create it](https://www.ias.edu/math/computing/faq/local-latex-style-files).

## Usage

The package can be loaded with a `pageno` option that enables page numbering. Be aware that, in order for the layout to display, your letter body should be wrapped in a `letterhead` environment.

Here is a minimal working example:

```tex
\documentclass{letter}
\usepackage{uvaletter}

\logo{logo.jpg}
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

The `\recipient{}` and `\department{}` fields are mandatory and must be non-empty.

In order for a logo to be displayed, you must indicate a path in `\logo{}`. The package is intended to be used with a logo from the University of Amsterdam. All official logos of the University, including its faculties, departments, and institutes, can be found [here](https://www.uva.nl/over-de-uva/over-de-universiteit/huisstijl/huisstijlelementen/logo/logo.html). If a path is not provided or the file is not found, the space reserved for the logo is left blank.

All other fields are optional.