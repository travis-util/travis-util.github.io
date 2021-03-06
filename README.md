# [travis-util.github.io](https://travis-util.github.io/)
Website for Travis-Util
* auto-gen TOC:
{:toc}

# Colorizing output

## Tools for colorizing

### Ccat
* jingweno/[ccat](https://github.com/jingweno/ccat)
* [ccat](https://google.com/search?q=ccat+site:debian.org)@site:debian

#### Supported file types
* .yml (YAML)
  - **Comments are unsupported**!

### Highlight
* travis-util/[highlight](https://github.com/travis-util/highlight)
* [highlight](https://tracker.debian.org/pkg/highlight)@debian

#### Unsupported file types
* .md
* .yml

### Pygments
* travis-util/[pygments-python-pip][]
* travis-util/[pygments-pip-not-python][]
* [Pygments][]@python

[pygments-python-pip]: https://github.com/travis-util/pygments-python-pip "GitHub"
[pygments-pip-not-python]: https://github.com/travis-util/pygments-pip-not-python "GitHub"
[Pygments]: https://pypi.python.org/pypi/Pygments "pypi.python.org"

### Source-highlight
* travis-util/[source-highlight](https://github.com/travis-util/source-highlight)
* [source-highlight](https://tracker.debian.org/pkg/source-highlight)@debian

#### Unsupported file types
* .md
* .yml

## File types to be colorized

### .html (HTML)
```sh
pygmentize -O linenos=1 <file>.html # Yet to test!
pygmentize -f html -O style=vim,linenos=1,full <file>.html | elinks -force-html -dump -dump-color-mode 1
```

### .js (Javascript)
```sh
pygmentize -P style=vim -f html -O full -P linenos=1 hello.js | elinks -force-html -dump-color-mode 1 -dump
```

### .md (Markdown)
* Why colorize? (Github makes it already! In edit mode...)

### .php (PHP)
```sh
php -s <file>.php | elinks -force-html -dump -dump-color-mode 1
```
* .php files are downloaded or produced by symfony/flex

### .py (Python)
```sh
pygmentize -O linenos=1 <file>.py
pygmentize -f html -O style=vim,linenos=1,full <file>.py | elinks -force-html -dump -dump-color-mode 1
```

### .yml (YAML)
```sh
pygmentize -O style=manni -f 256 <file>.yaml
pygmentize -f html -O style=vim,linenos=1,full <file>.yaml | elinks -force-html -dump -dump-color-mode 1
```
* .yml files are downloaded or produced by symfony/flex

# Deployment and repository update
* [travis update repository](https://www.google.ca/search?q=travis+update+repository)
* [*Deployment*](https://docs.travis-ci.com/user/deployment/)

## [GitHub Pages Deployment](https://docs.travis-ci.com/user/deployment/pages/)

## [GitHub Releases Uploading](https://docs.travis-ci.com/user/deployment/releases/)

# Windows with Wine
## Batch Scripting
### Intro and Syntax
* [run windows batch file on linux](https://google.com/search?q=run+windows+batch+file+on+linux)
* [*Batch_file*](https://en.wikipedia.org/wiki/Batch_file)
* [*Windows Batch Scripting*](https://en.wikibooks.org/wiki/Windows_Batch_Scripting)

### How to make them run
* [*Running Windows Batch Files on Linux*](https://www.linux.org/threads/running-windows-batch-files-on-linux.11205/)
* [*Run .bat in Linux environment*](https://stackoverflow.com/questions/12680998/run-bat-in-linux-environment)

# Travis configuration
## Multiline statements
### With `- |`
#### Example
```sh
- |
  composer create-project --no-install symfony/skeleton
  cd skeleton
  composer config bin-dir bin
  composer install
```
#### Documentation references
* [*How to escape indicator characters (i.e. : or - ) in YAML*](https://stackoverflow.com/questions/11301650/how-to-escape-indicator-characters-i-e-or-in-yaml)
## Multiline statements (oudated)
> Multiple lines can be made a single "virtual line" because of the way that
> Travis munges each line before executing it to print out the exit status.
> It's okay for it to be on multiple physical lines, so long as you remember:
> - There can't be any leading "-"s - All newlines will be removed, so use
> ";"s

* [nipy/dipy/.../.travis.yml](https://github.com/nipy/dipy/blob/master/.travis.yml)

Other references
* [travis multiline script @ Google](https://google.com/search?q=travis+multiline+script)
* *[How to use multiline command in 'script:' with YAML?](https://stackoverflow.com/questions/38745696/how-to-use-multiline-command-in-script-with-yaml)*
* [*Multi-line if statements in .travis.yml*](https://groups.google.com/forum/#!topic/travis-ci/uaAP9zEdiCg)
* [*Travis CI and If Statements*](http://steven.casagrande.io/articles/travis-ci-and-if-statements/)
* [*Writing a multiline command in configuration file*](https://discuss.circleci.com/t/writing-a-multiline-command-in-configuration-file/3042)

## Path
### Some directories in the PATH
* /home/travis/.local/bin (This directory does not exist).

# See also
* [github-wiki](https://github-wiki.github.io/)
* [symfony-util](https://symfony-util.github.io)
* [symfony-flex-demo](https://symfony-flex-demo.github.io)
