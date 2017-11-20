# travis-util.github.io
Website for Travis-Util
Colorizing output
=================
Tools for colorizing
--------------------
### Ccat
* jingweno/[ccat](https://github.com/jingweno/ccat)
* [ccat](https://google.com/search?q=ccat+site:debian.org)@site:debian
#### Supported file types
##### .yml (YAML)
* **Comments are unsupported**!
### Highlight
* travis-util/[highlight](https://github.com/travis-util/highlight)
* [highlight](https://tracker.debian.org/pkg/highlight)@debian
#### Unsupported file types
* .md
* .yml
### Pygments
* travis-util/[pygments-python-pip](https://github.com/travis-util/pygments-python-pip)
* travis-util/[pygments-pip-not-python](https://github.com/travis-util/pygments-pip-not-python)
* [Pygments](https://pypi.python.org/pypi/Pygments)@python
### Source-highlight
* travis-util/[source-highlight](https://github.com/travis-util/source-highlight)
* [source-highlight](https://tracker.debian.org/pkg/source-highlight)@debian
#### Unsupported file types
* .md
* .yml
File types to be colorized
--------------------------
### .html (HTML)
### .md (Markdown)
### .php (PHP)
```sh
php -s <file>.php | elinks -force-html -dump -dump-color-mode 1
```
### .py (Python)
### .yml (YAML)
