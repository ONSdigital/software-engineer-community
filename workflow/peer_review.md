# Creating a Pull Request (PR)
Once you have pushed a branch to GitHub you need to create a Pull Request in order for it to be reviewed and merged to master.

#### Definition
A code complete set of changes that in isolation can be merged into master without making it unstable or breaking other services.

* Reviewing open pull requests is more important than opening more pull requests
* More small pull requests are better than fewer large pull requests
* Understand the changes rather than assuming they are correct
* Automating styling checks is faster than manually style checking


#### The author should make it as easy as possible for a reviewer. They should:

* Add context
  - Why was the change made
  - What was changed
  - Link to relevant or related PRs
  - Link to issue trackers or other documentation e.g. Trello, Github issues, Confluence
* Explain how to review the changes
  - Steps to run tests
  - Steps to replicate or see changes
  - Add checklist for reviewer
* If the PR fixes an issue, add "fixes #issue-number" so that the issue is closed when the PR is merged

See https://github.com/ONSdigital/eq-survey-runner/pull/431 for an example of a good PR description.

#### Peer review requirements
* Changes can be merged into master without making it unstable
* Changes can be merged into master isolation without breaking other services
* Feature flags to disable changes that are not ready
* All code review comments are addressed or discussed
* Two code review approvals from people other than the author
* The code should contain no secrets
* Test coverage above threshold
* Ensure that any code changes are fully tested (via unit tests, acceptance tests etc.) and that all tests pass
* No linting issues
* Github integration checks pass

#### Considerations
* Avoid force pushing to a public branch (e.g. a pull request) while it's being worked on.
* It is ok to use the GitHub.com "Update" button whenever you like
* Code review comments should be logged against the PR in GitHub (rather than Slack).
* Any agreed changes (even if discussed in person) should be logged against the PR so anyone can see why changes are being made.
* Code reviews are an open forum, all comments are for discussion.
* Agreement must be met over comments for a PR to be merged.
* Involve a third party if agreement cannot be met.

#### When a PR is finished and ready for merging:

1. [Squash superfluous commits](squashing_commits.md) (wip, update after peer review etc)
1. If there are conflicts between master and your branch rebase master otherwise merge via the Github merge button (default option)
1. Merge changes by clicking the merge button and selecting `Squash and Merge`
