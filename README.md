# HYposter - LaTeX posters for University of Helsinki

HYposter is a style file for `beamerposter` whose purpose is to simplify the process
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
`olli.wilkman@iki.fi` and I will send the pdf logos to you and save you the trouble.

A version which allows eps logos is on the todo-list, but does not seem likely.

[beamer]: https://bitbucket.org/rivanvx/beamer/wiki/Home
[beamerposter]: http://www-i6.informatik.rwth-aachen.de/~dreuw/latexbeamerposter.php
[official graphics repository]: http://hy.logodomain.com/


## Usage

Once you have beamerposter and the template set up in your LaTeX installation or
working directory, using HYposter is fairly straightforward. Open one of the supplied
templates (either two- or three-column), and follow the five steps given in the template:

1. Choose the colour scheme.
2. Select your language.
3. Check that the file encoding is correct.
4. Fill in the title of your poster and your name
5. Add the contents of your poster

### Title lines

The title consists of two lines. The first one will be coloured in the faculty colour,
the second one in "silver". Due to technical limitations, you must give these two 
parts separately with the `\titlestart` and `\titleend` commands.

### Authors

Give the authors with the `\author` command. These are put to the right side of the title
in smaller black letters.

### Institute

The `\institute` command lets you specify another text block which will go below the
authors in slightly smaller font size.

### Bottom left corner

It's sometimes necessary to include things like logos of various institutes which have
supported or cooperated in the work. These kinds of things can be put in the lower
left corner of the poster with the `\leftcorner` command.

### Title size

Longer titles don't fit with the default size. If your title is long, you can use
the `\titlesize` command to change the size. The default is `\titlesize{\VeryHuge}`.
The best choice for a longer title is `\Huge`. If you need to go smaller than that,
your title is probably too long for a poster, but you can try `\LARGE`.

### Column length

The columns are essentially just vertical boxes. There is no wrapping over them,
which means that if you put too much stuff into a column, it will simply flow
over the bottom edge of the page. You must yourself make sure that your contents
fit the columns.

### Number of columns

The column width is fixed at the beginning by setting either `twocolumn` or `threecolumn`
(or nothing, which defaults to `threecolumn`) in the \usetheme options. This means that
you must use that number of `\newcolumn` commands to make the columns. Any less and you'll
have an empty space; any more, and the additionsl columns will go outside the page.


## Support

There are still various issues that could be better. If you have any suggestions or problems,
use the issue tracker for this project on Github, or [email me].

[email me]: mailto:olli.wilkman@iki.fi