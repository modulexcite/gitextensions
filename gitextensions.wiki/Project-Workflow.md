GitExtensions uses [semantic versioning](http://semver.org) for its releases. The basic workflow proceeds as follows.

1. General development work is performed on the **master** branch. During this time, new features may be added to the product.
2. In preparation for a release, a new branch is created with the name **release/<em>major</em>.<em>minor</em>**. For example, the branch **release/\<latest version\>** was created in preparation for the \<latest version\> release. These release branches are *feature frozen*; only small bug fixes are allowed to be added to one of these branches.

## Contributing to the Project

Contributions to the project are handled separately for new features and bug fixes.

### New Features

1. If an issue does not already exist for the feature, add one to the [issue tracker](https://github.com/gitextensions/gitextensions/issues). This allows the feature to be discussed, and eventually assigned to a particular release milestone.
2. Create a new lightweight branch in your fork of the project, which is based on the **master** development branch.
3. When you are ready to submit a pull request, submit the pull request using **master** as the base for the pull request. Provide screenshot for UI changes.

### Bug Fixes

1. If an issue does not already exist for the bug, add one to the [issue tracker](https://github.com/gitextensions/gitextensions/issues).
2. Choose a base branch for developing a fix for the bug. 
   1. Use **master** branch if bugfix contains a lot of changes.
   2. Check the [GitExtensions.releases](https://raw.github.com/gitextensions/gitextensions/configdata/GitExtensions.releases) document for the newest supported version of the software.
   3. Locate the newest release branch (highest version number) which exhibits the bug, but with the version listed in the GitExtensions.releases file. This is the base branch for your work. If no supported release branch exhibits the bug, the correction should be made to the **master** branch.
3. Like new features, you'll want to create a new lightweight branch in your fork of the project for bug fixes. We recommend naming the branch `fix-number`, where `number` is the issue number where the bug is reported. For example, a branch `fix-1960` could be used for fixing issue [#1960](https://github.com/gitextensions/gitextensions/issues/1960).

### Documentation

Update the documentation, or [raise an Issue](https://github.com/gitextensions/GitExtensionsDoc/issues/new) to indicate that documentation updates are required (see [Updating the Documentation](https://github.com/gitextensions/gitextensions/wiki#updating-the-documentation) for further details). 
