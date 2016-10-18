Git
---

Git is a distributed version control software to help a team cooperate and work together. The distributed part means that everyone has a copy of the full repository when working on it. Version controlled means all changes to the code are kept. This makes it simple to revert changes, see what has changed, and see who made the change. To get started you must install git on your computer.

`Installing Git`_

Configure
=========

Before using git you should set two values in the config. We need to tell git what your name is::

    git config --global user.name "John Doe"

And what your email is::

    git config --global user.email "John.Doe@example.org"

This is so git knows who is making the changes when you commit something to a repository. Github uses these values to assign a GitHub user to a commit so it is recommended that you use the same email address you used for signing up to Github.

Clone
=====

To be able to contribute you must first do what is called clone the repository. This will copy the repository from somewhere and make a local copy for you to edit::

    git clone https://github.com/fmuacm/alumniapp.git

This should create a folder in your current working directory called `alumniapp`. If you change directory to that folder you should see all the files that are listed on the main `alumniapp repository page`_\ . To read more go to `Git-SCM Clone Docs`_\ .

Add
===

So you have made some changes to your local repository. You will need to stage then commit your changes to your local repository so that git can keep track of them. If you do::

    git add somefile.txt

This will stage `somefile.txt` telling git there is a change I would like you to take note of. You can stage as many files as needed or just do::

    git add --all

This will tell git to stage all files. Git will look at every file and if it sees a change will stage it for you. To read more go to `Git-SCM Add Docs`_\ .

Commit
======

Staging tells git what you would like it to know about. Commiting is saying, these groups of changes are related and should be together. To commit your staged files do::

    git commit

This will open the command prompts default editor to ask for a commit message. Type in a nonempty commit message and save it. Your change is now committed to your local repository.

If you would like to skip the editor part you can do::

    git commit -m "Some message"

This will make the message of the commit `Some message`.

Your message should be a short description of what change you made. Good examples

- Updated API reference
- Edited README
- Added LICENSE
- Updated Terms Of Use

To read more go to `Git-SCM Commit Docs`_\ .

Status
======

Status is a simple command that lets you know what the status of your repository is. Are there any changes that are not staged to be committed? Are there any staged files ready to be committed? Is your repository up to date with the originating repository? To answer these questions simply run::

    git status

It is recommended that this command is used often so you know the state of your local repository at all times. To read more go to `Git-SCM Status Docs`_\ .

Log
===

Log lists all the commits that have been applied to your working copy of the repository. It will display the hash of all the commits (a unique identifier) and the commit message of each one. Simply run::

    git log

To read more go to `Git-SCM Log Docs`_\ .

Push
====

Now that you have committed your changes locally you would like for everyone else to have this change. You will need to push your changes to the originating repository. To do so do::

    git push

Things can get complicated here but this should work for the majority of the cases. To read more go to `Git-SCM Push Docs`_\ .

Pull
====

Either you have been away for a while, you want the latest and greatest, or you got an error when trying to push your changes to the originating repository and got an error. A simple fix is::

    git pull

This will get the latest changes from the originating repository and apply them to your local repository. You must not have any staged or unstaged changes (you can have commits that are not in the originating repository). Things can get complicated here as well but this should work for the majority of cases. To read more go to `Git-SCM Pull Docs`_\ .

Branching and Merging
=====================

This is a more advanced topic of git but I would like to describe the concept. A branch is what it sounds like, a branch off of the main code base. This is so you do not have to worry about changes to the main code branch until you are ready. The idea being you need to work on a feature that will take many commits to accomplish. You would create a branch from the code base and start working. Once you have everything working, on your branch, the way it should, you should merge your changes on top of the new code base (as it has probably changed since you made the branch).

A merge takes the changes not applied to your branch from the code base and tries to apply them. Git tries its best to resolve issues but sometimes it needs help. If a merge failed you can use `git status` to see which files need to be checked.

After a merge, you should test your feature again and any affected areas to make sure it is still working with the updated code base applied.

Some commands for branching and merging:

`git branch branchName`
    Create a branch called `branchName`

`git checkout branchName`
    Change to the branch `branchName`

`git checkout -b branchName`
    Create a branch called `branchName` and change to it

`git merge from into`
    merge the branch `from` into the branch `into`

To read more go to `Git-SCM Branch and Merge Docs`_

Further Reading
===============

`Git-SCM Docs`_ is a great place to learn more about git and the power it has.

Codeschool has a great interactive tutorial called `Try Git`_\ .

.. _Installing Git: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
.. _alumniapp repository page: https://github.com/fmuacm/alumniapp
.. _Git-SCM Clone Docs: https://git-scm.com/docs/git-clone
.. _Git-SCM Add Docs: https://git-scm.com/docs/git-add
.. _Git-SCM Commit Docs: https://git-scm.com/docs/git-commit
.. _Git-SCM Status Docs: https://git-scm.com/docs/git-status
.. _Git-SCM Log Docs: https://git-scm.com/docs/git-log
.. _Git-SCM Push Docs: https://git-scm.com/docs/git-push
.. _Git-SCM Pull Docs: https://git-scm.com/docs/git-pull
.. _Git-SCM Branch and Merge Docs: https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
.. _Git-SCM Docs: https://git-scm.com/doc
.. _Try Git: https://try.github.io
