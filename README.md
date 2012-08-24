CQLug Demo - August 2012
========================

## Goal

Provide a demo of how to create a simple pypi package for all your python scripts.

- Use github to store the source code for all your python scripts
- Use pypi to store an installable package containing all your custom python scripts
 - Conveniently pip install your package to any of your machines

## Creating Sources

The easiest way:

- Make a github account
- Fork an existing package that is similar (e.g. stonier/cqlug_demo)

Alternatively create a new repo and add some files to your package.
Some notes on the structure and the files you'll need for pypi packaging.

<pre>
 - setup.py : list of python files, meta info required for your pypi package
 - MANIFEST.in : describes what regular files should be added (e.g. docs)
 - Makefile : convenience build targets so you don't have to remember them
 - make.bat : same thing for windows
 - src/pkg_name/__init.py__ : python module header file (declares api)
 - src/pkg_name/*.py : python module files (module implementation)
 - src/scripts/* : executable python scripts
</pre>

The python scripts are most easily managed if they are almost empty and just
call your module api.

## Building

Two main use cases. While developing, it's easy to just install/uninstall directly.

<pre>
> make build
> sudo make install
# Test your python scripts
> sudo make uninstall
</pre>

## Creating the Package

- Create a pypi account.
- Register the package with pypi

 


