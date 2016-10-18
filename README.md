# Github Pages

This repository is for FMU ACM's Wiki. It uses Sphinx to render the docs from restructured text.

# Contributing

You will need to follow these instructions to get it running locally to transpile RST to HTML.

1. [Install Python](https://www.python.org/downloads/)

>**NOTE:** Either version is fine

2. [Install Pip](https://pip.pypa.io/en/stable/installing/) 

>**NOTE:** May already be installed if Python 2 >=2.7.9 or Python 3 >=3.4

3. [Install Sphinx](http://www.sphinx-doc.org/en/stable/install.html)
  * `pip install sphinx`
4. [Install Theme](https://github.com/snide/sphinx_rtd_theme)
  * `pip install sphinx_rtd_theme`

>**NOTE:** Windows Users: Pip requires administrative rights so make sure to run those commands in an administrative command prompt.

Edit the `*.rst` files in `src/source` to edit the wiki. `index.rst` is the table of contents file that is used to know what files to load (read more [here](http://www.sphinx-doc.org/en/stable/markup/toctree.html)).

You will need to transpile before pushing. Simply navigate into the `src` directory and run `make html`. This will recreate all the files for GitHub Pages.

>**NOTE:** Windows users run `.\make.bat clean & .\make.bat html`.

To test, simply navigate to this repository, and open the index.html file in a web browser.

## reStructuredText

I found [this](http://www.sphinx-doc.org/en/stable/rest.html) article to be useful. There are more options then this but it will get you started. 
