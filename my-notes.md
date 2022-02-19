# notes

```bash

Welcome to the Sphinx 4.4.0 quickstart utility.

Please enter values for the following settings (just press Enter to
accept a default value, if one is given in brackets).

Selected root path: .

You have two options for placing the build directory for Sphinx output.
Either, you use a directory "_build" within the root path, or you separate
"source" and "build" directories within the root path.
> Separate source and build directories (y/n) [n]:

The project name will occur in several places in the built documentation.
> Project name: rtd-rst-n2t
> Author name(s): multum-non-multa
> Project release []: 0.0.1

If the documents are to be written in a language other than English,
you can select a language here by its language code. Sphinx will then
translate text that it generates into that language.

For a list of supported codes, see
https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
> Project language [en]: en

Creating file readthedocs-rst-n2t/conf.py.
Creating file /readthedocs-rst-n2t/index.rst.
Creating file /readthedocs-rst-n2t/Makefile.
Creating file /readthedocs-rst-n2t/make.bat.

Finished: An initial directory structure has been created.

You should now populate your master file /readthedocs-rst-n2t/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

```

## again

```bash
# ran command
$ sphinx-quickstart docs


Creating file readthedocs-rst-n2t/docs/source/conf.py.
Creating file readthedocs-rst-n2t/docs/source/index.rst.
Creating file readthedocs-rst-n2t/docs/Makefile.
Creating file readthedocs-rst-n2t/docs/make.bat.

Finished: An initial directory structure has been created.

You should now populate your master file readthedocs-rst-n2t/docs/source/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. "html", "latex" or "linkcheck".

readthedocs-rst-n2t
├── README.rst
├── docs
│   ├── Makefile
│   ├── build
│   ├── make.bat
│   └── source
│       ├── _static
│       ├── _templates
│       ├── conf.py
│       └── index.rst
├── my-notes.md
├── poetry.lock
└── pyproject.toml

5 directories, 8 files
```

The purpose of each of these files is:

build/
An empty directory (for now) that will hold the rendered documentation.

make.bat and Makefile
Convenience scripts to simplify some common Sphinx operations, such as rendering the content.

source/conf.py
A Python script holding the configuration of the Sphinx project. It contains the project name and release you specified to sphinx-quickstart, as well as some extra configuration keys.

source/index.rst
The root document of the project, which serves as welcome page and contains the root of the “table of contents tree” (or toctree).

Thanks to this bootstrapping step, you already have everything needed to render the documentation as HTML for the first time. To do that, run this command:

```bash

$ sphinx-build -b html docs/source/ docs/build/html
# builds web-friendly files

 ```
