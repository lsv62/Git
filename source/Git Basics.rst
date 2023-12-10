Git Basics
==========

Getting a Git Repository
------------------------

Initializing a Repository in an Existing Directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

    git init

Do  an  initial  commint:

.. code-block::

    git add *.rst
    git commit -m 'Initial project version'

Cloning an Existing Repository
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Git  receives  a  full  copy  of  nearly  all  data  that the  server  has. 

.. code-block::

    git clone https://github.com/lsv62/SW400pro.git

Recording Changes to the Repository
-----------------------------------

Checking the Status of Your Files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

    git status

Tracking New Files
~~~~~~~~~~~~~~~~~~

.. code-block::

    cd sourse
    git add ProGit.rst

Staging Modified File
~~~~~~~~~~~~~~~~~~~~~

Short Status
~~~~~~~~~~~~

Ignoring Files
~~~~~~~~~~~~~~

Patterns for .gitignore

* blank lines or lines starting with # are ignored
* end patterns with a forward slash (/) to specify a directory
* negate a pattern by starting it with an exclamation point (!)
* an asterisk (*) matches zero or more characters
* [abc] matches any character inside the bracket
* a question mark (?) matches a single characte
* two asterisks to match nested directories `a/**/z`

Viewing Your Staged and Unstaged Change
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To know exactly what you changed before staging use the git diff command: 

.. code-block::

    git diff

To compare what is in your working directory with what is in your staging area.

.. code-block::

    git diff --staged

Committing Your Changes
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

    git commit -m "add comment to commit"

To commit changis without staging use following:

.. code-block::

    git commit -a -m "commit without staging"
    
Removing Files
~~~~~~~~~~~~~~

Remove readme.md file from disk

.. code-block::

    rm readme.md

And add it removing to stage 

.. code-block::

    git rm readme.md

To remove file just from staing area 

.. code-block::

    git rm --cached readme.md

Moving Files
~~~~~~~~~~~~

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

Limiting Log Output
~~~~~~~~~~~~~~~~~~~

Undoing Things
--------------

Unstaging a Staged File
~~~~~~~~~~~~~~~~~~~~~~~

Undoing things with git restore
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Unstaging a Staged File with git restor
"""""""""""""""""""""""""""""""""""""""

Unmodifying a Modified File with git restore
""""""""""""""""""""""""""""""""""""""""""""

Working with Remotes
--------------------

Showing Your Remotes
~~~~~~~~~~~~~~~~~~~~

Adding Remote Repositories
~~~~~~~~~~~~~~~~~~~~~~~~~~

Fetching and Pulling from Your Remotes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Pushing to Your Remotes
~~~~~~~~~~~~~~~~~~~~~~~

Inspecting a Remote
~~~~~~~~~~~~~~~~~~~

Renaming and Removing Remotes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Tagging
-------

Listing Your Tags
~~~~~~~~~~~~~~~~~

Creating Tags
~~~~~~~~~~~~~

Annotated Tags
~~~~~~~~~~~~~~

Tagging Later
~~~~~~~~~~~~~

Sharing Tags
~~~~~~~~~~~~

Deleting Tags
~~~~~~~~~~~~~

Checking out Tags
~~~~~~~~~~~~~~~~~
