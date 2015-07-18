Many research projects in the sciences use LaTeX, the well-known
typesetting software. This is excellent for writing papers, but at
earlier stages of projects it can feel like overkill.

*ProjectHugo* is a lightweight alternative that provides some of the
same functionality as LaTeX, but is intended for use at earlier,
organizational stages of projects.  It uses the static site generator
[Hugo](http://gohugo.io) to convert Markdown files to nicely formatted
HTML and CSS, including LaTeX support via MathJax.

## Getting Started

First, install git and the latest version of Hugo. If you're on a Mac,
this can be done easily using the [Homebrew](http://brew.sh) package
manager.

Next, become familiar with Markdown and MathJax, if you're
not already. For the basics, see below.

Now navigate to the directory where you want to put your project, and then
clone this repository by running

    git clone https://github.com/jhhalverson/ProjectHugo.git MyFolder

where *MyFolder* is replaced by the name of your project. Then run

    cd MyFolder

to navigate into that folder. Run

    hugo server --watch

to start the Hugo server. Navigate to the website the it recommends
(it likely has "localhost" in it) and get a feel for what's possible.
We will henceforth call this url "theurl".

Note that you can edit the .md files in the parts folder and Hugo will
(assuming that the server is still running with "--watch" enabled)
reload the web browser in automatically. If you use an editor that
auto saves, this allows you to write in real time, equations and all.

## Using ProjectHugo

Using ProjectHugo is just like using Hugo. If you want a comprehensive
introduction, visit the [Hugo website](http://gohugo.io/). Here are
the basics, though.

First, you will write all of your ProjectHugo content in the folder
"parts" and its subfolders. Suppose you're working on a project that
involves magnetic monopoles, and you wanted to collect your notes,
thoughts, and calculations on magnetic monopoles in a particular file.
There are two basic ways in which you might want to proceed. If you
expect this to be a simple part of your project, use

    hugo new monopoles.md

which will create monopoles.md in your parts folder. Edit this file
in your favorite editor and, with the Hugo server running navigate
to *theurl/monopoles/*. The page will be reloaded any time you
save the source file monopoles.md.

Alternatively, for a larger part of the project you might want a
dedicated subdirectory. To do this, run

    hugo new monopoles/index.md

and a new file will be create the file *parts/monopoles/index.md*.
Edit this file and, with the Hugo server running, you'll be able to
view it at *theurl/monopoles/*. Since there is a subdirectory
monopoles, you may want related files to go in there. For example

    hugo new monopoles/dirac.md

or

    hugo new monopoles/thooft-polyakov.md

for different types of monopoles that you might want to study. The
first would appear at *theurl/monopoles/dirac/*, for example. I like
this "extra subdirectory" approach because I often have other files
(SAGE, Mathematica, etc) associated with a particular part of a
project.

## Markdown and MathJax

Markdown is a plain-text markup language that is transformed by Hugo
into the web page that you view in your browser. For an introductinon
to Markdown, [see here](https://help.github.com/articles/markdown-basics/).

MathJax is a javascript library that renders many LaTeX-formatted
equations into proper equations on webpages. For an introduction to
MathJax,
[see here](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference),
for example.

## Custom Commands

Some custom LaTeX commands often used in the physics literature are
implemented in ProjectHugo. For an up-to-date list, examine the source
in *layouts/_default/single.html*.
