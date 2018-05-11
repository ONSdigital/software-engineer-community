# Continuous Integration
Changes merged into master will be deployed automatically and tested. Preventative action should be taken to prevent merging changes that could fail continuous integration.

#### Failing Continuous Integration
When CI fails it should be classed as a high priority to fix and make it stable again. This is because:

* It will block the flow of the pipeline potentially blocking production releases
* Developers will be blocked to prevent compounding the issue

##### Actions

1. Make the team aware of failure
1. Re-run tests check if it's a flaky test (If it is flaky schedule time to fix it)
1. Triage issue to get an understanding of why it's failing
1. Fix code changes and raise a pull request
1. Consider backing out the changes if the fix will take a long time
1. Write tests to catch the failures earlier in the process

#### Before raising a Pull Request
It is important to remember how code changes could affect the continuous integration environment. e.g. Jenkins, Concourse

Any CI changes should be made as early as possible, ideally before raising a pull request.

#### Examples of CI changes that could be made independently before merging any code changes are:
 
* Adding/Changing environmental variables
* Adding a new service
* Adding a new Cloudfoundry service
* Changing the versions of the build tools used
* A github repository is renamed

#### Examples of CI changes which may need to be updated after merges are:

* Build scripts added/removed
* Changing the build tools used
* Removing a service
* A change to how the tests run

#### After merging a Pull Request
Close attention should be made to CI. Any failure from the build of a service or test should be investigated and resolved immediately.