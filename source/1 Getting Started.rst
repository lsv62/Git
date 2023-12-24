
Getting Started
===============

What is Git?
------------

Snapshots
~~~~~~~~~

Every time you commit Git save snapshot that contains all changes in files references to previous snapshot 
fir files that isn't chnaged.

Nearly Every Operation Is Local
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Nealy all operations on Git is local and doesn't depend upon network even for hystory of project.
If you offline you can commit and save changes when you get to net later.

The Three State
~~~~~~~~~~~~~~~

:Modified:
    File has a changing

:Staged:
    File choosed and marked to include in next commit

:Commited:
    File saved in local database

First-Time Git Setup
--------------------

.. glossary:: 

    ``config``
        lets you get and set configuration variables that control all aspects of how Git looks and operate

    ``config --system``
        in [path]/etc/gitconfig contains configuration for all users

    ``config --global``
        in [user]/.gitconfig contains configuration for user

    ``config --local`` 
        in .git/config that configuration for repo

    ``config --local --list --show-origin``
        show local config

    ``config --list``
        see all your configs

Your Identity
~~~~~~~~~~~~~

.. glossary:: 

    ``config --global user.name "..."``
        set your user name that necessary for commits

    ``config --global user.email ...``
        set your e-mail that necessary for commits

Getting Help
------------

.. glossary:: 

    ``help config``
        getting offline help

    ``config -h``
        getting brief help

