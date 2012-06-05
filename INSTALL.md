# Installing HYposter

## The easiest way

You can use HYposter simply by keeping the `beamerthemeHYposter.sty` file in your
working directory, and keeping the flame logo(s) you need in a subdirectory called 
`flames`.

If you also lack `beamerposter`, get the `beamerposter.sty` file from [here] and
keep it in your working directory as well. This will of course only allow you to 
use the style with LaTeX documents located in that specific directory.


**IMPORTANT:** Some LaTeX distributions include `beamerposter`, but a very
old version (v1.07), which does not work with this poster style. 
HYposter is guaranteed to work only with `beamerposter` v1.12!
If your `beamerposter` is too old, you will get a warning like this: `LaTeX 
Warning: You have requested, on input line 3, version '2010/11/18' of package 
beamerposter, but only version '2008/03/11. v.1.07. beamerposter: latex-beamer
poster extension' is available.`


[here]: http://www-i6.informatik.rwth-aachen.de/~dreuw/latexbeamerposter.php

## The better way

The preferred method is to add the style to your LaTeX distribution so that
it is usable everywhere. The specific way to do this depends on your system.

On some LaTeX distributions there are tools to install packages. Some even
automatically download missing packages from CTAN, which takes care of
`beamerposter`, but you still need to install `HYposter`. Below are the manual
steps to do it.

Your LaTeX packages are located under a directory called `texmf` somewhere
on your system. Where it is exactly depends on your system and your 
LaTeX distribution. You need to find it yourself.

The actual steps to install both `beamerposter` and `HYposter` are:

1. Copy `beamerposter.sty` and `beamerthemeHYposter.sty` into a directory called `texmf/tex/latex/beamerposter/`. 
2. Copy the flame graphics into `texmf/tex/latex/beamerposter/flames/`. 
3. On most systems: run `texhash` or some other tool (again, depending on your
LaTeX distribution) to re-index the texmf directory so that LaTeX knows where to
look for the packages.

If you have Mac OS X and the MacTeX distribution, the `texmf` directory for user
packages is `~/Library/texmf/` and one does not need to rehash anything.

## The power user way

If you want to mess around with the style yourself, I suggest forking
the project on Github, git-cloning it to some suitable directory and instead of
copying, simply adding a symlink of `beamerthemeHYposter.sty` in `texmf/tex/latex/beamerposter`,
then re-index the LaTeX distribution if necessary.