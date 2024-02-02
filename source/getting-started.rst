
Getting Started
===============

What is Git?
------------
git 
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

    configuration for all users
        ``git config --system -l`` in [path]/etc/gitconfig

    configuration for user
        ``git config --global -l`` in [user]/.gitconfig

    configuration for repo
        ``git config --local -l`` in .git/config that 

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

