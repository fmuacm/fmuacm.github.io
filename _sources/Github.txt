Github
------

Github is an online repository for users who are using the git version control software. It allows contributors to pull and push to and online repository with ease.

Please read the `Git Docs`_ to learn more about git.

The following is broken down into the tabs for any given repository.

Code
====

Is the main view of the repository. If a `README` file is present, GitHub will render the text in HTML. It can render markdown and reStructuredText depending on the extension of the README file.

Code shows the root of the repository. You can click on a file or folder to view its content. If you have write access you may edit it in the browser but it is not recommended to do so.

Issues
======

"Issues are used to track todos, bugs, feature requests, and more." Just as GitHub says issues are pretty much anything about the current state of the repository. An issue can have a label to mark what kind of issue it is (highly recommended so sorting is easier).

You may assign an issue to a user so we know who is working on the issue. This is helpful to help not step on everyone's foot.

Issues help make the workflow of the repository more simple. Create a bunch of feature issues. Then start assigning them to yourself when you get to them. When you are done you can close the issue stating that it is in the main branch. If for some reason you are done with the issue but can't put it in the main branch, a best practice is to add a label to that issue saying it is done just not published yet. 

Pull Requests
=============

Pull requests are a way for contributors to review code changes before being merged into the main branch. This allows catching mistakes or improvements before moving forward.

To create a pull request simply push a new branch up to Github::

    git push -u origin someBranch

The `-u` tells git to remember this while I am on this branch. This will make a new branch in Github. Navigate to the repositories main page and you will see a dialog saying that it realized you pushed to a new branch and is asking if you want to create a pull request. Create the pull request. Give the pull request a meaningful title and a brief description of what you did in the branch.

Contributors are now able to review and comment ideas or concerns. If they think it is fine they should leave a comment saying that it looks good. After a few people have reviewed and said it looked fine you should feel comfortable with your changes and merge them into the main branch.

Further Reading
===============

It may be helpful to comment an issue in a commit message or pull request title/message. You can do so by just using its reference number (IE `#23`). If the commit fixes an issue you should use a convention from `Github's Closing Issue By Reference`_\ . So when the commit or pull request is merged or pushed to the default branch the issue will close automatically.

Github has great documentation on how to use some of its features located in `Github Help`_\ .

.. _Git Docs: https://github.com/fmuacm/alumniapp/wiki/Github
.. _Github's Closing Issue By Reference: https://help.github.com/articles/closing-issues-via-commit-messages/
.. _Github Help: https://help.github.com/