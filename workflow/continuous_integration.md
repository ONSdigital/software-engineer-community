# Continuous Integration (CI)
Changes merged into master should be deployed automatically and tested. Preventative action should be taken to prevent merging changes that could fail continuous integration.

## Failing Continuous Integration
When CI fails it should be classed as a high priority to fix and make it stable again. This is because:

* It may block the flow of the pipeline potentially blocking production releases
* It may prevent other developers from getting accurate feedback from the pipeline for their changes

## Actions

1. Make the team aware of failure e.g. stand-ups, Slack, dashboard, shouting
1. Re-run tests check if it's a flaky test (if it is flaky schedule time to fix it)
1. Triage the issue to get an understanding of why it's failing
1. Consider backing out the changes if the fix will take a long time
1. Write tests to catch the failures earlier in the process
1. Fix code changes and raise a pull request

## Before raising a Pull Request
It is important to remember how code changes could affect continuous integration.

Any CI changes should be made as early as possible, ideally before raising a pull request.

## Examples of CI changes that could be made independently before merging any code changes are:

* Adding/changing environment variables
* Adding a new service
* Adding a new Cloudfoundry service
* Changing the versions of the build tools used
* A Git repository is renamed

## Examples of CI changes which may need to be updated after merges are:

* Build scripts added/removed
* Changing the build tools used
* Removing a service
* A change to how the tests run
