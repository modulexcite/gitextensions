The following explains how to update the documentation for the **current** release of Git Extensions. The **current** release of Git Extensions is the release that is available for download on the SourceForge site.

## Verify Update Required
Firstly, verify that the documentation update is still required i.e. that it has not already been fixed. The version of the documentation distributed with the Git Extensions download may be out of date. Please check the latest version of the documentation at the [Read the Docs](https://git-extensions-documentation.readthedocs.org/en/latest/) website. 

Also check any [open Issues] (https://github.com/gitextensions/GitExtensionsDoc/issues) in the GitExtensionsDoc repository to see if it has already been raised.

## Raise an Issue
Raise an Issue that explains the problem with the documentation. Please ensure you state that the Issue raised relates to the currently released version of the documentation.

If you don't want to modify the documentation yourself, then this is all that is required.

## Modifying Documentation
Once you have raised an Issue (or selected an Issue if you want to work on a currently open one) then update the issue to say you are working on it. 

To update the the documentation, you will need to have a GitHub account. You can then:
- fork the [GitExtensionsDoc](https://github.com/gitextensions/GitExtensionsDoc) repository
- make a local clone on your machine
- create a new branch based on the **'latest'** branch. It can be called anything you like
- make your documentation updates on this new branch
- push the branch to your GitHub fork
- create a Pull Request, specifying the Head repo/Head branch as the repository/branch in your GitHub fork containing the documentation updates, and the Base repo/Base branch as GitExtensionsDoc/latest.

This Pull Request will then be reviewed by the documentation maintainers and actioned if there are no queries. It will be merged into the 'latest' branch to update the latest documentation available at Read the Docs and also the 'master' branch to ensure any future releases also contain this update.   

## For Developers
If you are a developer who is coding a 'bugfix' to the current release, then please refer to the [Future Release](Future-Release) page as, until patches to individual releases are implemented, your bugfix is considered a future release. 