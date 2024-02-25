Основи Git
==========

Як працює Git
----------------

.. glossary::

    ``git workflow``
        * Створіть repository (проект) за допомогою інструменту new сайті github
        * Скопіюйте (clone) репозиторій на вашу локальну машину
        * Додайте файл до свого локального репо та commit (збережіть) зміни
        * Push ваші зміни до основної гілки
        * Внесіть зміни у свій файл за допомогою інструмента хостингу git і commit
        * Pull зміни на вашу локальну машину
        * Створіть branch (версію), внесіть зміни, commit зміни
        * Відкрити pull request (запропонувати зміни до головної гілки)
        * Merge свою гілку з головною гілкою

Отримання репозиторію Git
-------------------------

Ініціалізація репозиторію в існуючому каталозі
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ця команда створює каталог .git із підкаталогами для об’єктів, посилань/заголовків, 
посилань/тегів і файлів шаблонів, а також початкову гілку без будь-яких комітів.

.. glossary::

    ``init``
        Запустити контроль версій за допомогою Git
        
Клонування існуючого сховища
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``clone https://github.com/<repository>``
        Копія існуючого сховища git
        
    ``clone -l <local path>``
        Клонувати з локального сховища
        
Якщо репозиторій вказано як локальний шлях (наприклад, /path/to/repo), 
то -l ігнорується.

.. glossary::

    ``clone --single-branch``
        Клонувати лише одну гілку, на яку вказує HEAD або параметр --branch
       
    ``clone -b``
        Клонувати віддалену гілку замість HEAD
        
Після клонування git fetch без аргументів оновить усі гілки віддаленого відстеження, 
а git pull без аргументів додатково об’єднає віддалену головну гілку в поточну головну гілку.

Ця конфігурація досягається шляхом створення посилань на головки віддалених гілок у 
refs/remotes/origin та шляхом ініціалізації змінних конфігурації remote.origin.url і 
remote.origin.fetch.

Запис змін до репозиторію
-----------------------------------

Перевірка стану ваших файлів
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``status``
        відображає шляхи, які мають відмінності між файлом індексу та поточним комітом HEAD, 
        шляхи, які мають відмінності між робочим деревом та файлом індексу, 
        і шляхи в робочому дереві, які не відстежуються Git.
        
    ``status -s``
        відображає скорочено cтан скорочено стан індексу і стан робочого директорія:

        * M оновлено в індексі
        * T тип змінено в індексі
        * А додано до індексу
        * D видалено з індексу
        * R перейменовано в індексі
        * C скопійовано в індекс
        
    ``status -b master``
        відображає cтан гілки master
        
    ``status --ignored``
        відображає cтан ігнорованих файлів

Відстеження нових файлів
~~~~~~~~~~~~~~~~~~~~~~~~~

«Індекс» містить знімок вмісту робочого дерева, і саме цей знімок береться як вміст 
наступного коміту.

.. glossary::

    ``add <file>``
        розпочати відстеження нового файлу
   
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

Перегляд позначених для коміту файлів
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``diff``
        Зміни між робочим деревом та індексом
        
    ``diff --cached``
        Зміни між індексом і останнім комітом
      
    ``diff HEAD``
        Зміни між робочим деревом та останнім комітом   
        
    ``diff AUTO_MERGE``
        Зміни в робочому дереві після вирішення текстових конфліктів
        
    ``diff topic master``
        Зміни між topic та master гілками
        
        
Закріплення ваших змін
~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``commit -m "commit message"``
        Внести зміни
      
    ``commit Makefile``
        Внести зміни до Makefile
        
    ``commit --amend``
        Змінити попередній комміт
        
    ``get commit -a``
        Внести зміни з попереднім додаванням в індекс файлів, які були змінені та видалені
    
.. image:: _static/Transport-command.png

Видалення файлів
~~~~~~~~~~~~~~~~~

.. glossary::

    ``rm <file>``
        Видаляє файли з робочого дерева та з індексу

    ``rm --cached <file>``
        видаляє файл лише з індексу; робочі файли, змінені чи ні, залишаться в спокої.

Переміщення иа перейменування файлів
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``mv <file_from> <file_to>``
        перейменування файлу

    ``mv <file> ... <directory>``
        переміщення файлу в діректорію

Перегляд історії комітів
--------------------------

.. glossary::

    ``log``
        перераховує коміти, зроблені в цьому сховищі, у зворотному хронологічному порядку

    ``log - p``
        показати зміни, внесені кожним комітом

    ``log -2``
        показати 2 остнніх коміта

    ``log --pretty=oneline``
        друкує кожен коміт в одному рядку

Limiting Log Output
~~~~~~~~~~~~~~~~~~~

.. glossary::

    ``log --since=2.weeks``
         list of commits made in the last two week

    ``log -- <path/to/file>``
         limit the log output to commits that introduced a change to those file

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
