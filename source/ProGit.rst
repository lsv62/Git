
Getting started
===============

Snapshots
---------

Every time you commit Git save snapshot that contains all changes in files references to previous snapshot 
fir files that isn't chnaged.

Local Operations
----------------

Nealy all operations on Git is local and doesn't depend upon network even for hystory of project.
If you offline you can commit and save changes when you get to net later.

Only Adds Data
--------------

After you commit snapshot it's very difficult to lose data especially if you refularly push your database to another repo.

File states
-----------

:Modified:
    File has a changing

:Staged:
    File choosed and marked to include in next commit

:Commited:
    File saved in local database

The Command Line
----------------

The command line is the only place you can use all git command.

Git Setup
---------

git config let you get to 3 configuration files

* --system in [path]/etc/gitconfig that contains configuration for all users
* --global in [user]/.gitconfig that contains confu=iguration for user
* --local in .git/config that contains configuration for repo

To show local config for example use following:

.. code-block::

    git config --local --list --show-origin

Or if you want to see all your configs:

.. code-block::

    git config --list

Your Identity
-------------

Every  Git  commit  uses  this  information

.. code-block::

    git config --global user.name "LSV"
    git config --global user.email lsv@kotris.ua

Getting Help
------------

Use git help For offline help as in example:

.. code-block::

    git help config

or -h key for brief help:

.. code-block::

    git config -h

Git Basics
==========

Initializing a Repository in an Existing Directory
--------------------------------------------------

.. code-block::

    git init

Do  an  initial  commint:

.. code-block::

    git add *.rst
    git commit -m 'Initial project version'

Ignoring Files
--------------

Patterns for .gitignore

* blank lines or lines starting with # are ignored
* end patterns with a forward slash (/) to specify a directory
* negate a pattern by starting it with an exclamation point (!)
* an asterisk (*) matches zero or more characters
* [abc] matches any character inside the bracket
* a question mark (?) matches a single characte
* two asterisks to match nested directories `a/**/z`

Cloning an Existing Repository
------------------------------

Git  receives  a  full  copy  of  nearly  all  data  that the  server  has. 

.. code-block::

    git clone https://github.com/lsv62/SW400pro.git

Checking the Status of Your Files
---------------------------------

.. code-block::

    git status

Tracking New Files
------------------

.. code-block::

    cd sourse
    git add ProGit.rst

Viewing Your Staged and Unstaged Change
---------------------------------------

To know exactly what you changed before staging use the git diff command: 

.. code-block::

    git diff

To compare what is in your working directory with what is in your staging area.

.. code-block::

    git diff --staged

Committing Your Changes
-----------------------

.. code-block::

    git commit -m "add comment to commit"

To commit changis without staging use following:

.. code-block::

    git commit -a -m "commit without staging"
    