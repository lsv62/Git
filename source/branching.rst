
Створення нової гілки (версії)
----------------------------------

.. glossary::

    ``branch``
        * ``<branch name>`` - створює новий ``HEAD`` на поточний комміт, але не переключилися на нього
        * ``-d <branch name>`` - видаляє гілку
        * ``-v`` - виводить останній commit з кожної гілки
        * ``--merged`` - виводить гілки вже об’єднані з поточною.
         Гілки в цьому списку без * перед ними зазвичай можна видалити

    ``branch --no-merged``
        see all the branches that contain work you haven’t yet merge

    ``branch -D <branch name>``
        delete unmerged branch

    ``branch --all``
        lists both the local and the remote tracking branches

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



Basic Merge Conflicts
~~~~~~~~~~~~~~~~~~~~~

Git adds standard conflict-resolution  markers  to  the  files  that  have  conflicts,  
so  you  can  open  them  manually  and resolve those conflicts.

Branch Management
-----------------

.. glossary::



Changing a branch name
~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``branch --move old-branch-name new-branch-name``
        replaces  your  branch name  locally

    ``push --set-upstream origin new-branch-name``
        replaces  your  branch name  remotely

    ``push origin --delete <branch-name>``
        delete remote branch

Branching Workflows
----------------------

Long-Running Branches
~~~~~~~~~~~~~~~~~~~~~~~~

..glossary::

    Developers workflow 
        * having only stable code in master  branch
        * another branch to work, test stability and if stable  merge  into  master
        * other  branches at various levels of stability merge into the branch above

Topic Branches
~~~~~~~~~~~~~~~~

Remote Branches
---------------

.. glossary::

    ``git ls-remote <remote>``
        get a full list of remote references

    ``<remote>/<branch>``
        remote-tracking  branches - references to the state of remote branches when its was conncted the last time

    ``remote  show  <remote>``
        get a full list of remote references

    ``fetch  <remote>``
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
        