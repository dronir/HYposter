# HYposter - LaTeX posters for University of Helsinki

This is a style file for `beamerposter` whose purpose is to simplify the process
of making scientific posters that have a University of Helsinki look with LaTeX.
HYposter tries to look like the "tighter" version of the official poster style.

`beamerposter` is a LaTeX package which uses `beamer` for typesetting posters.

HYposter is based on the Icy theme by Philippe Dreuw, although diverging rapidly.

## Requirements

LaTeX with [beamer] and [beamerposter]. Most modern LaTeX installations come with
`beamer` included, but you must install `beamerposter` yourself.

You also need pdf versions of the University of Helsinki flame logos for each
faculty. Unfortunately these can't be provided here as they are under copyright.
If you are university staff, you can get them (like I did) by downloading them
from the [official graphics repository]. Unfortunately they are mostly not
available in pdf format, so you must download them in some other format and
convert and rename. They are available in eps format, but for some reason
the epstopdf tool crashes on some of them.

Aternatively, if you are university staff, send a request to me at
olli.wilkman@iki.fi and I will send the pdf logos to you and save you the trouble.

A version which allows eps logos is on the todo-list.

[beamer]: https://bitbucket.org/rivanvx/beamer/wiki/Home
[beamerposter]: http://www-i6.informatik.rwth-aachen.de/~dreuw/latexbeamerposter.php
[official graphics repository]: http://hy.logodomain.com/

## Installation

You can use HYposter either by keeping the `beamerthemeHYposter.sty` file in the
directory where you are working, and keeping the flame logo(s) you need in a
subdirectory called `flames`.

The preferred method is to add the style to your LaTeX distribution so that
it is usable everywhere. The specific way to do this depends on your system.
Do this manually by copying `beamerthemeHYposter.sty` to a directory called
`texmf/tex/latex/beamerposter/` and putting the flame graphics in
`texmf/tex/latex/beamerposter/flames/`. The location of the `texmf`
directory depends on your system. You may need to run `texhash` or something
to make LaTeX find it after this.

Note that if you have installed `beamerposter` properly, then `beamerposter.sty`
should also be in `texmf/tex/latex/beamerposter/`.

On Mac OS X and the MacTeX distribution the `texmf` directory is `~/Library/texmf/` 
and one does not need to rehash anything.

Pro option: If you want to mess around with the style yourself, I suggest forking
the project on Github, cloning it to some suitable directory and adding symlinks 
to the file in `texmf/tex/latex/beamerposter`.

## Usage

Once you have beamerposter and the template set up in your LaTeX installation,
using HYposter is fairly straightforward. Open one of the supplied templates (either
two- or three-column), and follow the five steps given in the template:

1. Choose the colour scheme.
2. Select your language.
3. Check that the file encoding is correct.
4. Fill in the title of your poster and your name
5. Add the contents of your poster as `block` environments.