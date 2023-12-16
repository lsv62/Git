Git Basics
==========

Getting a Git Repository
------------------------

Initializing a Repository in an Existing Directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``init``
        start version  control with  Git

Cloning an Existing Repository
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``clone https://github.com/<repository>``
          copy of an existing git repository and sets up local master to track remote

Recording Changes to the Repository
-----------------------------------

Checking the Status of Your Files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``status``
         determine which files are in which stage

Tracking New Files
~~~~~~~~~~~~~~~~~~

.. glossary::

    ``add <file>``
         begin  tracking  a  new  file

Short Status
~~~~~~~~~~~~

.. glossary::

    ``status -s``
          see  your  changes  in  a  more  compact  way

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

.. glossary::

    ``diff``
        see what you’ve changed but not yet staged

    ``diff --staged``
        compare what is in your working directory with what is in your staging area

Committing Your Changes
~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``commit -m "commit message"``
         commit changes

Skipping the Staging Area
~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``commit -a -m "commit message"``
        commit changis without staging
    
Removing Files
~~~~~~~~~~~~~~

.. glossary::

    ``rm <file>``
         stages the file’s removal

    ``rm --cached <file>``
        remove from staging area accidently staged file 

Moving Files
~~~~~~~~~~~~

.. glossary::

    ``mv <file_from> <file_to>``
        renave file and add to stage

Viewing the Commit History
--------------------------

.. glossary::

    ``log``
        lists  the  commits  made  in  that  repository  in  reverse chronological order

    ``log - p``
        Show the patch introduced with each commit.

    ``log --pretty=oneline``
        prints each commit on a single line

Limiting Log Output
~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``log --since=2.weeks``
         list of commits made in the last two week

    ``log -- path/to/file``
         limit the log output to commits that introduced a change to those file

Undoing Things
--------------

.. glossary::

    ``commit --amend``
         amend  last local commit

Unstaging a Staged File
~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``reset HEAD <file>``
         unstage the file

Unmodifying a Modified File
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``checkout -- <file>``
        discard changes in working directory

Undoing things with git restore
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``restore --staged <file>``
        unstage file

    ``restore <file>``
        discard the changes in file

Working with Remotes
--------------------

Showing Your Remotes
~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``remote -v``
        shows you the remote server URLs

Adding Remote Repositories
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``remote add <shortname> <url>``
        add  a  new  remote  Git repository as a shortname you can reference easily

Fetching and Pulling from Your Remotes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``fetch origin``
        download data from remote clone repository

    ``pull``
        fetch and merge remote branch to your current branch

Pushing to Your Remotes
~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``push origin master``
        push your master branch to your  origin  server (you'll have to fetch first if someone else push upstream before)

Inspecting a Remote
~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``remote show origin``
        lists the URL for the remote repository as well as the tracking branch information

Renaming and Removing Remotes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``remote rename <old name> <new name>``
        change a remote's shortname

    ``remote remove <name>``
         remove a remote

Tagging
-------

Listing Your Tags
~~~~~~~~~~~~~~~~~

.. glossary::

    ``tag``
        listing your Tags

Annotated Tags
~~~~~~~~~~~~~~

.. glossary::

    ``tag -a <tagname> -m "tag message"``
        Create  an  annotated  tag

    ``show <tag version>``
        see the tag data along with the commit that was tagged

Lightweight Tags
~~~~~~~~~~~~~~~~

.. glossary::

    ``tag <tagname>``
         tag commits with a lightweight tag

Tagging Later
~~~~~~~~~~~~~

.. glossary::

    ``tag -a <tagname> <part of commit checksum>``
         tag commit with the commit checksum

Sharing Tags
~~~~~~~~~~~~

.. glossary::

    ``push origin <tagname>``
         transfer tags to remote server

    ``push origin --tags``
         a lot of tags to push up at on server

Deleting Tags
~~~~~~~~~~~~~

.. glossary::

    ``tag -d <tagname>``
         delete  a  tag  on  local  repository

    ``push origin --delete <tagname>``
         remove the tag from any remote servers

Checking out Tags
~~~~~~~~~~~~~~~~~

.. glossary::

    ``checkout <tagname>``
         view the versions of files a tag is pointing t
