
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

git config let you get to 3 configuration files

.. glossary:: 

    git config
        lets you get and set configuration variables that control all aspects of how Git looks and operate

    git config --system 
        in [path]/etc/gitconfig contains configuration for all users

    git config --global 
        in [user]/.gitconfig contains confu=iguration for user

    git config --local 
        in .git/config that configuration for repo

    git config --local --list --show-origin
        show local config

    git config --list
        see all your configs

Your Identity
-------------

.. glossary:: 

    git config --global user.name "LSV"
        set your user name that necessary for commits

    git config --global user.email lsv@kotris.ua
        set your e-mail that necessary for commits

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
    
Removing Files
--------------

Remove readme.md file from disk

.. code-block::

    rm readme.md

And add it removing to stage 

.. code-block::

    git rm readme.md

To remove file just from staing area 

.. code-block::

    git rm --cached readme.md

Viewing the Commit History
--------------------------

Option of Git log

.. code-block::

    - p Show the patch introduced with each commit.
    --stat Show statistics for files modified in each commit.
    --shortstat Display only the changed/insertions/deletions line from the --stat command.
    --name-only Show the list of files modified after the commit information.
    --name-status Show the list of files affected with added/modified/deleted information as well.
    --abbrev-commit Show only the first few characters of the SHA-1 checksum instead of all 40.
    --relative-date Display the date in a relative format (for example, “2 weeks ago”) instead of
        using the full date format.
    --graph Display an ASCII graph of the branch and merge history beside the log output.
    --pretty Show commits in an alternate format. Option values include oneline, short,
        full, fuller, and format (where you specify your own format).
    --oneline Shorthand for --pretty=oneline --abbrev-commit used together.

Undoing Things
--------------
