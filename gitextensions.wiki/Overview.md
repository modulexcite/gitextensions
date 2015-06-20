The documentation for Git Extensions is held in a [separate repository](https://github.com/gitextensions/GitExtensionsDoc) from the code repository. The documentation consists of a number of text files written in ReStructuredText (.rst) format, along with image files in Portable Network Graphics (.png) format. The ReStructuredText files are processed using the Sphinx Python Documentation Generator.

The documentation can be generated locally, using scripts supplied as part of the repository. Note that certain pre-requisites are required for this, including Python 2.x and Sphinx. Sphinx supports various output formats including PDF, HTML (separate and one single HTML file) and Microsoft Help format. The documentation can also be generated automatically at the Read the Docs website, ensuring that the online documentation is always up to date.

## Branches
The documentation repository consists of two permanent branches: master and latest.

### Branch: master
This branch reflects the state of the documentation that incorporates **all** changes. Any modifications to documentation for the *current* release of Git Extensions and modifications for *future* releases of Git Extensions should be contained in this branch.

### Branch: latest
This branch reflects the state of the documentation for the **latest** release of Git Extensions only. The latest release of Git Extensions is that which is available at the official [SourceForge](http://sourceforge.net/projects/gitextensions/) link.

When any changes are merged into this branch, the online documentation at Read the Docs is automatically generated.

## Read the Docs
The [Read the Docs](https://readthedocs.org/) website allows for the generation of Sphinx documentation written in ReStructuredText format. A Service Hook has been enabled for the GitExtensionsDoc repository such that when commits are made to the repository, the Read the Docs website is notified and, if the commit is to the 'latest' branch, the documentation is automatically regenerated.

This means the online documentation for the currently released version of Git Extensions is always up to date. The latest documentation in HTML format can be found [here](https://git-extensions-documentation.readthedocs.org/en/latest/).

Read the Docs also generates the documentation in various other formats automatically. These can be downloaded from [here](https://readthedocs.org/projects/git-extensions-documentation/downloads/). Note that some of these document formats may or may not generate correctly - the content will be there but the formatting of the document may not be correct.

## Directory Structure and Files
The GitExtensionsDoc repository has the following directory structure.

### GitExtensionsDoc
This is the root directory. Files in this directory include the Windows ``.cmd`` files that, when run, will generate various versions of the Git Extensions manual e.g. HTML, Windows Help, PDF, etc.  

### GitExtensionsDoc/source
This directory contains the ``.rst`` files. These are the ReStructuredText files that are processed by Sphinx and formatted into the Git Extensions manual.

### GitExtensionsDoc/source/images
This directory contains images that are used in the Git Extensions manual e.g. screen prints.

### GitExtensionsDoc/source/images/code_repo
This directory contains images copied directly from the GitExtensions code repository that are used in the manual. If any of these images are updated in the code repository, then they should also be updated in this directory. The files here have the same name as in the code repository and may be found in the following directory:
* ``gitextensions/GitUI/Resources/Icons`` 

### GitExtensionsDoc/source/images/*
All other sub-directories under images contain images used in various chapters of the manual.

### GitExtensionsDoc/source/nature2
This directory contains the 'theme' that is used when the manual is generated as HTML (either via the ``.cmd`` files or on the Read the Docs site).

## Useful Links
- to generate documentation locally, [Python 2.x](http://www.python.org/) i.e. latest 2.x version, is needed, as well as Sphinx. Once Python is installed, the Python Package Manager can be used to install Sphinx and any required dependencies by opening a Command Prompt window and entering at the command prompt:
 
          pypm install sphinx

- to create files that Sphinx can process, refer to the [Sphinx documentation](http://sphinx-doc.org/contents.html) for the syntax of .rst files.
- see this [online ReStructuredText editor](http://rst.ninjs.org/) that, via a split screen, allows you to enter ReStructuredText markup and immediately see the results.    

## Future
In the future, it is anticipated that
- the documentation supplied with a release of Git Extensions will consist of a single HTML file (instead of the current PDF documentation)
- the GitExtensionsDoc repository will support multiple Git Extensions releases via the use of specific release branches (as per the code repository).
