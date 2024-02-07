Основи Git
==========

Отримання репозиторію Git
-------------------------

Ініціалізація репозиторію в існуючому каталозі
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    Запустити контроль версій за допомогою Git
        ``git init``

Cloning an Existing Repository
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    Копія існуючого репозиторію git
        ``git clone https://github.com/<repository>``

    Клонувати з локального сховища
        ``git clone -l``

    Клонувати лише одну гілку, HEAD або --branch
        ``git clone --single-branch``

    Клонувати віддалену гілку замість HEAD
        ``git clone -b``

Запис змін до репозиторію
-----------------------------------

Перевірка стану ваших файлів
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    Статус файлів
        ``git status``

    Статус коротко 
        ``git status -s``

    Статус гілки
        ``git status -b``

    Статус ігнорованих файлів
        ``git status --ignored``

Відстеження нових файлів
~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    розпочати відстеження нового файлу
        ``git add <file>``

Ігнорування файлів
~~~~~~~~~~~~~~~~~~

Шаблони для .gitignore

* порожні рядки або рядки, що починаються з #, ігноруються
* шаблони закінчуються скісною рискою (/), щоб вказати каталог
* заперечувати шаблон, починаючи його зі знака оклику (!)
* зірочка (*) відповідає нулю або більше символів
* [abc] відповідає будь-якому символу в дужках
* знак питання (?) відповідає одному символу
* дві зірочки для відповідності вкладених каталогів `a/**/z`

Перегляд позначений для коміту файлів
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    змінені, але не помічені для коміту файли
        ``git diff``

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

    ``log -- <path/to/file>``
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

    origin
        name Git gives to the server you cloned from

    ``remote -v``
        shows you the remote server URLs with reading and writing access

Adding Remote Repositories
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``remote add <shortname> <url>``
        add  a  new  remote  Git repository as a shortname you can reference easily

Fetching and Pulling from Your Remotes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``fetch origin``
        download references to all the branches from remote to merge in or inspect

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
         view the versions of files a tag is pointing to
