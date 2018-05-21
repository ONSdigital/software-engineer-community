# Commit Messages

## Writing good commit messages
Use the imperative mood in the subject line. Verbose descriptions should be on subsequent lines (i.e. like an e-mail subject and body).
Good commit messages describe what has changed and the rationale behind those changes.

* Separate subject from body with a blank line
* Limit the subject line to 50 characters
* Capitalize the subject line
* Do not end the subject line with a period
* Use the imperative mood in the subject line
* Wrap the body at 72 characters
* Use the body to explain what and why vs. how
* Link to issue tracker

## Blogs and examples

* http://chris.beams.io/posts/git-commit
* https://github.com/ONSdigital/eq-survey-runner/commit/71a164749e7b9db6089bd7ec608305bb6d667b1d
* https://github.com/ONSdigital/eq-survey-runner/commit/660c9f14352e4f9b4f5eb9cfdab212a14996f77b

## What's in a commit

* The commit should contain changes that are described in the commit message
* If changes are not described in a commit message it could probably be in another commit
* Changes should compile
* Changes should pass unit tests
* Changes should pass linting

## Pushing to GitHub

Before pushing to GitHub for the first time (making it public); consider rebasing your branch to master to pick up the latest changes and resolve any conflicts.

```bash
git checkout eq-123-signon
git pull --rebase origin master
git push origin eq-123-sign-on

```
