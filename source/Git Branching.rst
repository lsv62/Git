
Git Branching
=============

Branches in a Nutshell
----------------------

Commit object in Git repository contains: 

    * commit object with  the  pointer  to  directory  tree  and  all  the  commit metadata;
    * tree that lists the contents of the directory and specifies which file names are stored as blobs;
    * blobs representing the contents of the files.

Creating a New Branch
~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``branch <branch name>``
        creates a new pointer called  ``HEAD`` to the commit you’re currently on but didn’t switch to 

Switching Branches
~~~~~~~~~~~~~~~~~~

.. glossary::

    ``switch <branch name>``
        switches to an existing branch, moves HEAD to the branch and change file in working directory

    ``switch -c <newbranchname>``
        Creating a new branch and switching to it at the same time

    ``switch -.``
        Return to your previously checked out branch

Basic Branching and Merging
---------------------------

Basic Branching
~~~~~~~~~~~~~~~

It’s best  to  have  a  clean  working  state  by commiting changes when  you  switch  branches.

.. glossary::

    ``merge <branch name>``
        merge the branch back into current branch

    ``branch -d <branch name>``
        delete branch

Basic Merging
~~~~~~~~~~~~~

Basic Merge Conflicts
~~~~~~~~~~~~~~~~~~~~~

Branch Management
-----------------

Branching Workflows
-------------------

Remote Branches
---------------

Rebasing
--------
