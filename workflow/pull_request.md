# Creating a pull request
Once you have pushed a branch, a pull request (merge request in GitLab) should be created to allow the changes to be reviewed by the team before it's merged to master.

## Definition
A code complete set of changes that **in isolation can be merged into master without making it unstable or breaking other services**.

* Reviewing code is more important than creating more code to review
* Many small pull requests are better than fewer large pull requests
* Understanding the changes rather than assuming they are correct
* Automating styling checks rather than manually style checking

## The author should make it as easy as possible for a reviewer. They should:

* Add context
  - Why was the change made
  - What was changed
  - Link to relevant or related pull requests
  - Link to issue trackers or other documentation e.g. Trello, Github issues, GitLab issues, Confluence
* Explain how to review the changes
  - Steps to run tests
  - Steps to replicate or see changes
  - Add checklist for reviewer
* If the pull request fixes an issue, add "fixes #issue-number" so that the issue is closed when the pull request is merged

See https://github.com/ONSdigital/eq-survey-runner/pull/431 for an example of a good pull request description.

## Peer review requirements
* Changes can be merged to master without making it unstable
* Changes can be merged to master isolation without breaking other services
* Feature flags to disable features that are not ready
* All pull request comments are addressed or discussed
* Two pull request approvals from people other than the author
* The code or documentation should contain no secrets
* Test coverage above a threshold agreed by the team
* Ensure that any code changes are fully tested (via unit tests, acceptance tests etc.) and that all tests pass
* No linting issues
* Github integration checks pass

## Considerations
* Avoid force pushing to a public branch (e.g. a pull request) while it's being worked on.
* Frequently merge changes from master into your branch
* Pull request comments should be logged against the pull request (rather than Slack).
* Any agreed changes (even if discussed in person) should be logged against the pull request so anyone can see why changes are being made.
* Pull requests are an open forum, all comments are for discussion.
* Agreement must be met over comments for a pull request to be merged.
* Involve a third party if agreement cannot be met.

## When a pull request is finished and ready for merging:

1. [Squash superfluous commits](squashing_commits.md) (wip, update after peer review etc)
1. Keep the branch up to date by rebasing master onto your branch
1. If there are conflicts between master and your branch resolve them running the tests to confirm nothing is broken
1. Merge changes
    - In Github click the merge button dropdown and select `Squash and Merge`
