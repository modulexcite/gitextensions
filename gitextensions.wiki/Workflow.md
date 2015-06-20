This is the workflow that the GitExtensionsDoc repository maintainers should follow to ensure all documentation updates are applied correctly.

## Processing Pull Requests
Pull Requests will relate to documentation for the currently released version or future versions of Git Extensions. These requests are processed as follows:
- a Pull Request for the currently released version will be merged into the 'latest' branch. This will cause the documentation at Read the Docs to be automatically rebuilt. The 'latest' branch should always be merged into 'master'. 
- a Pull Request for a future version will be merged into the 'master' branch **once** the associated code has been accepted in the code repository.

## Performing a Major Release
When the Git Extensions code is ready for the next major release, then
- create a major release branch e.g. release/X.yy from the 'master' branch
- update the ``version`` and ``release`` variables in the ``conf.py`` configuration file to reflect the major release number
- the documentation packaged with the release can be built from this branch via the scripts in the documentation repository e.g. create a single HTML file for inclusion in the release
- when the software is released on SourceForge, merge the release/X.yy branch into the 'latest' branch. Documentation at Read the Docs will be automatically rebuilt and this branch now reflects the currently released version.

## Future
It is proposed that minor releases (bugfixes) be applied to major releases (see [this Issue](https://github.com/gitextensions/gitextensions/issues/1458)). This workflow will be modified accordingly if this Issue is implemented.
