Many research projects in the sciences use LaTeX, the well-known
typesetting software. This is excellent for writing papers, but at
earlier stages of projects it can feel like overkill.

*ProjectHugo* is lightweight alternative that provides some of the
same functionality as LaTeX, but is intended for use at earlier,
organizational stages of projects.  It usese the static site generator
Hugo to convert Markdown files to nicely formatted HTML and CSS,
including LaTeX support via MathJax.

## Getting Started

First, install git and the latest version of Hugo. If you're on a Mac,
this can be done easily using the [Homebrew](http://brew.sh) package manager.

Navigate to the directory where you want to put your project, and then
clone this repository by running

    git clone https://github.com/jhhalverson/ProjectHugo.git MyFolder

where *MyFolder* is replaced by the name of your project. Then run

    cd MyFolder

to navigate into that folder. Run

    hugo server --watch

to start the hugo server.
