# phd-prelim-research

Richard Wen  
rwen@ryerson.ca  

* [Slides](https://rrwen.github.io/phd-prelim-research)
* [PDF](https://github.com/rrwen/phd-prelim-research/blob/master/slides/wen2018_phd_prelim_research_slides.pdf)

Preliminary PhD research.

[![Build Status](https://travis-ci.org/rrwen/phd-prelim-research.svg?branch=master)](https://travis-ci.org/rrwen/phd-prelim-research)
[![GitHub license](https://img.shields.io/github/license/rrwen/phd-prelim-research.svg)](https://github.com/rrwen/phd-prelim-research/blob/master/LICENSE)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/rrwen/phd-prelim-research.svg?style=social)](https://twitter.com/intent/tweet?text=Preliminary%20PhD%20research:%20https%3A%2F%2Fgithub.com%2Frrwen%2Fphd-prelim-research%20%23revealjs%20%23slides)

## Install

1. Install [npm](https://www.npmjs.com/)
2. [Clone](https://git-scm.com/docs/git-clone) this repository
3. Install dependencies with `npm`

```
git clone https://github.com/rrwen/phd-prelim-research
cd phd-prelim-research
npm install
```

See [Edits](#edits) and [Implementation](#implementation) for more details.

## Usage

1. Generate `docs/index.html` (see `script.html` in [package.json](https://github.com/rrwen/phd-prelim-research/blob/master/package.json))
2. Generate `slides/wen2018_phd_prelim_research_slides.pdf` (see `script.pdf` in [package.json](https://github.com/rrwen/phd-prelim-research/blob/master/package.json))

```
npm run html
npm run pdf
```

## Developer Notes

### Edits

The following can be edited before generating:

* `slides/wen2018_phd_prelim_research_slides.md`: [Markdown](https://daringfireball.net/projects/markdown/) file with slide contents
* `slides/template.html`: Custom [reveal-md](https://github.com/webpro/reveal-md) template to generate slides with
* `docs/edit/style.css`: [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) file to adjust styling of slides
* `docs/edit/logo.png`: logo image to use

### Implementation


The slides [phd-prelim-research](https://github.com/rrwen/phd-prelim-research) uses the following [npm](https://www.npmjs.com/) packages for its implementation:

npm | Purpose
--- | ---
[reveal-md](https://www.npmjs.com/package/reveal-md) | Converting `slides/wen2018_phd_prelim_research_slides.md` to `docs/index.html`
[decktape](https://www.npmjs.com/package/decktape) | Converting `slides/wen2018_phd_prelim_research_slides.md` to `slides/wen2018_phd_prelim_research_slides.pdf`
[windows-build-tools](https://www.npmjs.com/package/windows-build-tools) | Compiling dependencies for decktape on Windows Operating System (OS)

```
       reveal-md            <-- Convert markdown  slides to html

       decktape             <-- Convert markdown slides to pdf
          |
  windows-build-tools       <-- Compile decktape on Windows OS
```
