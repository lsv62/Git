
Getting Started
===============

Snapshots
---------

Every time you commit Git save snapshot that contains all changes in files references to previous snapshot 
fir files that isn't chnaged.

Local Operations
----------------

Nealy all operations on Git is local and doesn't depend upon network even for hystory of project.
If you offline you can commit and save changes when you get to net later.

File states
-----------

:Modified:
    File has a changing

:Staged:
    File choosed and marked to include in next commit

:Commited:
    File saved in local database

Git Setup
---------

.. glossary:: 

    ``git config``
        lets you get and set configuration variables that control all aspects of how Git looks and operate

    ``git config --system``
        in [path]/etc/gitconfig contains configuration for all users

    ``git config --global``
        in [user]/.gitconfig contains configuration for user

    ``git config --local`` 
        in .git/config that configuration for repo

    ``git config --local --list --show-origin``
        show local config

    ``git config --list``
        see all your configs

Your Identity
-------------

.. glossary:: 

    ``git config --global user.name "LSV"``
        set your user name that necessary for commits

    ``git config --global user.email lsv@kotris.ua``
        set your e-mail that necessary for commits

Getting Help
------------

.. glossary:: 

    ``git help config``
        getting offline help

    ``git config -h``
        getting brief help

