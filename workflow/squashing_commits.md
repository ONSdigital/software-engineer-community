# Squashing commits 

```bash
git fetch origin master && git rebase -i origin/master
```
Will start an interactive rebase on all the commits that are on your branch but not master. Note this will squash out merge commits automatically.

An interactive rebase will give you an editor like below

```
pick 522e40b Correcting spelling mistake
pick e552aef Adding new unit test
pick 05cbee3 DIGEQ-7 review questionnaire functionality
# Rebase 26823ee..05cbee3 onto 26823ee
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out
```
Choose the commits you wish to squash. The below example shows the last 2 commits being squashed into the first commit.

```
pick 522e40b Correcting spelling mistake
squash e552aef Adding new unit test
squash 05cbee3 DIGEQ-7 review questionnaire functionality
# Rebase 26823ee..05cbee3 onto 26823ee
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out
```
Save this and allow git to perform the rebase, it will then prompt you to select a commit message

```
# This is a combination of 3 commits.
# The first commit's message is:
Correcting spelling mistake

# This is the 2nd commit message:
Adding new unit test

# This is the 3rd commit message:
DIGEQ-7 review questionnaire functionality

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# rebase in progress; onto 520a0cf
# You are currently editing a commit while rebasing branch 'squashing' on '520a0cf'.
#
# Changes to be committed:
#       modified:   survey/models.py
#       modified:   survey/tests/test_questionnaire.py
#       modified:   templates/survey/questionnaire_detail.html
#
```
You should write a commit message which will describe the change appropriately.

```
DIGEQ-7 review questionnaire functionality
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# rebase in progress; onto 520a0cf
# You are currently editing a commit while rebasing branch 'squashing' on '520a0cf'.
#
# Changes to be committed:
#       modified:   survey/models.py
#       modified:   survey/tests/test_questionnaire.py
#       modified:   templates/survey/questionnaire_detail.html
```
The history should now be

```
commit 05cbee3b8c6d6909f35f0cdcd7b1dc44add5bb86
Author: Warren <warren@methodsdigital.co.uk>
Date:   Wed Sep 30 10:37:08 2015 +0100

    DIGEQ-7 review questionnaire functionality

commit 26823ee53df97b511ef7e9e728112b90086b4508
Merge: f017d12 338bd77
Author: Dan Hilton <daniel.hilton@gmail.com>
Date:   Tue Sep 29 22:21:52 2015 +0100
    Merge pull request #23 from ONSdigital/digeq-8-make-questionnaire-live

    Publish a questionnaire

```

If you have already pushed up your commits and by squashing them you will be rewritten the history on the remote you will need to force push your changes. When force pushing changes you should **triple check** and then check again as you will potentially overwrite other peoples changes. This should almost never be done on master.

```bash
git push origin <branch> -f
```
