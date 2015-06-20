If you are a developer who is modifying the Git Extensions code repository to either fix bugs in the latest release or write new features *and* these code changes affect the documentation, then please follow the procedures below.

## Raise an Issue
As a developer, you are encouraged to modify the documentation yourself (as you know better than anyone how your changes affect the documentation). If you do not wish to update the documentation, then please raise an Issue in the [Git Extensions Doc repository](https://github.com/gitextensions/GitExtensionsDoc/issues). This Issue should:
- reference the Pull Request in the code repository that implements your bug fix/new feature
- adequately explain how the code change affects the documentation e.g. adding/modifying options in a dialog, or how the behaviour of Git Extensions has changed that impacts an explanation in the documentation

Anybody can then update the documentation as per your explanation.
        
## Modifying Documentation
To modify the documentation yourself, you will need to 
- fork/clone the [GitExtensionsDoc](https://github.com/gitextensions/GitExtensionsDoc) repository
- create a new branch based on the 'master' branch (since any code changes you are doing are for a future release of Git Extensions, the documentation updates are also for a future release). The branch name should probably reflect the branch name created in the code repository e.g. branch feature/new-feature-desc in code repo should be feature/new-feature-desc-doc in documentation repo.
- update the documentation on this branch in your clone
- push to your documentation fork and raise a Pull Request in the GitEXtensionsDoc repository. In this Pull Request, also reference the code repository branch/Pull Request

The GitExtensionsDoc Pull Request will then be reviewed by the documentation maintainers and merged into the 'master' branch if there are no issues. This merge will probably not be done until the code branch is merged into 'master' in the code repository - this ensures the documentation reflects an accepted feature.
