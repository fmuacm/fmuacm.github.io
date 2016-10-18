GoLang
------

GoLang is a language inspired by other languages. It is a fairly new language. It will take a little bit of getting used to but the best part is you can cross compile. Like Java, it can run on many platforms. But unlike Java, you do not need a runtime to be installed on the machine you are executing the application on. The binary that is compiled is statically compiled meaning that no outside dependency libraries are required on the client machine.

Installing
==========

Installing GoLang is pretty straight forward. Follow the instructions at `GoLang Install Docs`_\ .

Configure
=========

This is where most people have an issue. You do have GoLang installed but your environment is not set up completely yet. You need to setup your `GoLang Workspace`_\ .

After doing so you will need to set an environment variable named `GOPATH` so GoLang knows where everything is. It is recommended that you add `$GOPATH/bin` to your `PATH` as well. Read more about `GOPATH` at `GoLang Gopath`_\ .

Running
=======

GoLang has a simple command called `run` that will compile your go program and run it. To do so run::

    go run main.go

Of course, GoLang looks for the package `main` and the function `main` to find its entry point.

Building
========

Building a binary in GoLang is as simple as calling::

    go build import/path

This will create a binary that has the name of the root directory.

Installing Packages
===================

GoLang has many packages built in. But if you want a package someone else made you simply run::

    go get import/path

This assumes that the package is on GitHub by the user `user` and the repository `package`. This is great for developers to be able to create an open source package and distribute it with ease.

Format
======

GoLang comes with a nifty command called `fmt`. Run it by running::

    go fmt import/path

This will format your code to a standard. It is recommended running this before pushing to the repository so everyone is using the same formatting standards.

Import Path
===========

Import path is how GitHub knows where to get the package from. Your local workspace mimics this by using folders under `$GOPATH/src`. But for you to be able to create a package you need to follow a rule. The path needs to be an URL to the package minus the protocol. Example::

    https://www.github.com/fmuacm/alumniapp     #url
    github.com/fmuacm/alumniapp                 #import path

Using that convention go will know where to get the package if you do not already have that installed locally.

Further Reading
===============

`GoLang Docs`_ has some great information on how to program in GoLang.

I have found `Go By Example`_ really helpful when trying to figure out the proper syntax for certain tasks.

There are a lot of videos on youtube with a few tutorials of GoLang! This `Youtube GoLang Playlist` seems to cover most of GoLang.

.. _GoLang Install Docs: https://golang.org/doc/install
.. _GoLang Workspace: https://golang.org/doc/code.html#Workspaces
.. _GoLang Gopath: https://golang.org/doc/code.html#GOPATH
.. _GoLang Docs: https://golang.org/doc/
.. _Go By Example: https://gobyexample.com/
.. _Youtube GoLang Playlist: https://www.youtube.com/playlist?list=PL2ANXDJvvFeJLRIL_8NZl5LGtrRE3sE_E