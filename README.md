# LaTeX-beamer-Hokie
If you are into using the [LaTeX Beamer class](http://en.wikipedia.org/wiki/Beamer_%28LaTeX%29) for creating your presentations, and you are a Hokie, then this theme is for you!

This is a LaTeX Beamer class style that uses the official VT color palette (i.e., the one used throughout VT's websites), includes the VT logo, and provides example code for Beamer class presentations. 

This theme can be used for presentations given internally, or for slides presented at conferences. A number of students have used this theme for their thesis / dissertation defense.

## What does it look like?

You can obviously use whatever inner / outer theme you like, but this is what the default looks like:

## Included Files
This repository contains two subdirectories:

* `beamerhokie` - This is the actual Beamer theme.
* `beamer-example` - This is just an example presentation that demonstrates how to use the theme, and what it looks like.

This distribution contains 3 LaTeX *.sty files:

* `beamercolorthemeHokieColors.sty`
    This file defines colors based on the VT Web Color Palette Guidelines. All
    of the colors are defined using RGB values, and assigned to English-language
    names. Note that very few of these colors are actually used in the provided
    theme - they are defined for your use, in case you want to use them on your
    own.

* `beamercolorthemeHokieLayout.sty`
    This style file assigns the defined Hokie Colors to various aspects of the
    slides, defines the bullet point shape and color for {itemize} environments,
    defines some font colors, etc.

* `beamerthemeHokie.sty`
    This file defines the inner and outer slide theme, pulls in the Hokie Colors
    definitions, and makes other presentation-wide declarations.  This theme
    file is what enables the \usetheme{Hokie} command.

* png logo files
    These are logo files with backgrounds that match the default background
    canvas setting in beamercolorthemeHokieLayout. Right now there is the
    generic VT logo, and one for Wireless@VT.


## Using the Theme
For now, there is no installation.  Put the style files in your project
directory, and include the  following directive under your
\documentclass{beamer} declaration, but before \begin{document}:

    \usetheme{Hokie}

## Using a Logo
If you want to use one of the logos in your slides, include the following code
between \documentclass{beamer} and \begin{document}:

    \graphicspath{{./}}  % Assuming the themes are in the local directory
    \DeclareGraphicsExtensions{.png}
    \logo{\includegraphics[height=0.5cm]{vt-logo.png}}
    \setbeamertemplate*{logo}

Note that the 'graphicx' package is included by default in beamer-class
documents.

## Extra Instructions
The theme provides for a number of feature usage, and things actually look 
somewhat strange if you DON'T use them.  Make sure, for example, that you set 
your organization with the institution command - otherwise, there will be an 
empty set of parenthesis at the bottom of your slides:

    \institute{Virginia Tech}

Also, remember that you can easily change the default font of your slides. I've 
found that things look awesome with the Palatino font:

    \usepackage{palatino}

## LICENSE
All code is released under the GNU GPL v3.
