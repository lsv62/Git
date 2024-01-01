
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

Basic Merge Conflicts
~~~~~~~~~~~~~~~~~~~~~

Git adds standard conflict-resolution  markers  to  the  files  that  have  conflicts,  
so  you  can  open  them  manually  and resolve those conflicts.

Branch Management
-----------------

.. glossary::

    ``branch -v``
        To  see  the  last  commit  on  each branch

    ``branch --merged``
        see which branches are already merged into the branch you’re on.
        Branches on this list without the * in front of them are generally fine to delete

    ``branch --no-merged``
        see all the branches that contain work you haven’t yet merge

    ``branch -D <branch name>``
        delete unmerged branch

Changing a branch name
~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``branch --move old-branch-name new-branch-name``
        replaces  your  branch name  locally

    ``push --set-upstream origin new-branch-name``
        replaces  your  branch name  remotely

    ``push origin --delete <branch-name>``
        delete remote branch


Remote Branches
---------------

.. glossary::

    ``remote  show  <remote>``
        full list of remote references

    ``fetch  origin``
        synchronize  local  with  a  remote

Pushing
~~~~~~~

.. glossary::

    ``push <remote> <branch>``
         push branch up to remote

    ``merge origin/<branch>``
        merge remote branch into your current working Branch

    ``checkout -b <branch> origin/<branch>``
        getting local copy of  remote-tracking branch

Tracking Branches
~~~~~~~~~~~~~~~~~

.. glossary::

    ``checkout --track origin/<branch>``
        set  up  tracking  branch

    ``branch -u origin/<branch>``
          set remote <branch> to the same local for tracking

    ``branch -vv``
        see what tracking branches you have set upstream. 
        This command’s telling you about what it has cached from these servers locally

    ``fetch --all``
         totally up to date ahead and behind from all your remotes
         
Rebasing
--------

The Basic Rebase
~~~~~~~~~~~~~~~~

.. glossary::

    ``rebase <branch>``
        replays  changes  from  one  line  of  work  onto  another  in the order they were introduced, 
        whereas merging takes the endpoints and merges them together
        