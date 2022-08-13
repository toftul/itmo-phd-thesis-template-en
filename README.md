# PhD Thesis template for ITMO University

This is not an official template. It works fine with [Overleaf](https://www.overleaf.com/). 

If you are writing your dissertation in Russian, there is [toftul/itmo-phd-thesis-template-ru](https://github.com/toftul/itmo-phd-thesis-template-ru).

## Why does this exist

There is an official template on the [ITMO Dissertation Council](https://dissovet.itmo.ru/index.php?main=110) website, which is a fork of the well-known template [AndreyAkinshin/Russian-Phd-LaTeX-Dissertation-Template](https://github.com/AndreyAkinshin/Russian-Phd-LaTeX-Dissertation-Template). 

However both these templates are extremely overloaded and it's hard to use them without much experience in programming and $\LaTeX$. In addition, there are many features (beamer, docker, separate compilation of the synopses, the choice of different engines of bibliography, etc.), which are usually useless while writing a dissertation at ITMO. Turns out you can throw out more than half of them, which has been done.

## What has changed

1. Removed all the files you won't need when compiling in Overleaf. Also all folders with documentation and GOST are removed;
2. Removed the choice between `bibtex` and `biblatex` in favor of the latter one, because it is the most modern version of the bibliography engine;
3. Abstract and Synopsys inserted into the main document, as required by the template ITMO;
4. Counters and output of own paper (how many in total, how many in Scopus, etc.) are done from sratch.

## How to use

### Start
* Download the `zip` of this repository;
* Upload it to [Overleaf](https://www.overleaf.com/).

### Literature
There are two files with literature (**I highly suggest doing bib entries via [BibItNow!](https://chrome.google.com/webstore/detail/bibitnow/bmnfikjlonhkoojjfddnlbinkkapmldg?hl=en-US)**):
1. `biblio/references.bib' is the standard bib file, where all the sources you are going to cite go, including your own work;
2. `biblio/own.bib` is the list of your articles and conferences. This file is used for the automatic output in the general thesis summary part. However, you will need to manually add the necessary `keywords` to make it work.

Example `keywords` are: 
* `own` is your article, not the conference;
* `wos` - Web if Science;
* `scopus` - Scopus;
* `vak` - VAK;
* `other` - article/proceedings from other sources;
* `conf` - conference.

Example of the bib-entry:
``bib
@article{Toftul2019Oct,
        keywords = {own, scopus, wos}, % <--- here!
        Author = {Toftul, I. D. and Bliokh, K. Y. and Petrov, M. I. and Nori, F.},
        title = {{Acoustic Radiation Force and Torque on Small Particles as Measures of the Canonical Momentum and Spin Densities}},
        journal = {Phys. Rev. Lett.},
        volume = {123},
        number = {18},
        pages = {183901},
        year = {2019},
        month = {Oct},
        issn = {1079-7114},
        publisher = {American Physical Society},
        url = {https://doi.org/10.1103/PhysRevLett.123.183901},
        doi = {10.1103/PhysRevLett.123.183901}
}

%Sorry for this but this works
@article{metanano2021,
        keywords = {conf}, % <--- here!
        author = {\textbf{METANANO}}
        year={2021},
        journal = {13-17 September 2021 Saint Petersburg, Russia (Online)},
        title = {{Two talks: High-Q states in acoustic apple-shaped resonators, Nonlinear circular dichroism in Mie-resonant nanoparticle dimers}}
}
```

### The rest

Everything else should be intuitive.
