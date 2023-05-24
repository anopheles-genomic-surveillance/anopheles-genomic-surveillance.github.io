# *Anopheles* genomic surveillance

This repository holds lecture notes for a training course on genomic surveillance of *Anopheles* mosquitoes, which are vectors of malaria.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a> This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

## Maintainer notes

### Checking the notebooks

Please see the video below for a guide to how to check the lecture notebooks for any problems and report any issues you find:

<iframe width="560" height="315" src="https://www.youtube.com/embed/DrVCqSrfAV8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Development environment setup

Here are instructions for getting set up to work on this project.

Fork this GitHub repository to your own GitHub account.

Clone your fork. E.g.:

```bash
git clone git@github.com:alimanfoo/anopheles-genomic-surveillance.github.io.git
cd anopheles-genomic-surveillance.github.io
```

Create a Python virtual environment to use as the development environment. There are various different ways to create a virtual environment. E.g., if you have virtualenvwrapper:

```bash
mkvirtualenv --python=/usr/bin/python3.7 anopheles-genomic-surveillance-dev
```

Then activate your development environment, e.g.:

```bash
workon anopheles-genomic-surveillance-dev
```

Then you can install requirements:

```bash
pip install -r requirements.txt
```

### Building the book

The training course website is built using jupyterbook. From your local clone of the repo, first ensure you have activated your development environment, e.g.:

```bash
workon anopheles-genomic-surveillance-dev
```

...then you can build the book:

```bash
jb build docs
```

This should render the book as HTML files. The command will show where
the HTML files have been created, so you can preview them in a
browser.

In some cases you may need to preview the HTML files via an HTTP
server. You can run an HTTP server locally with this command:

```bash
python -m http.server --directory docs/_build/html
```

