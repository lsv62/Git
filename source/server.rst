
Git on the Server
=================

The Protocols
-------------

Local Protocol
~~~~~~~~~~~~~~

.. glossary::

    ``clone <path>/.git``
          clone a local repository from <path>/.git to current folder

The HTTP Protocols
~~~~~~~~~~~~~~~~~~

Smart HTTP
""""""""""

.. glossary::

    Smart HTT
        use username/password  authentication

Dumb HTTP
"""""""""

.. glossary::

    Dumb HTTP
        expects the Git repository to be served like normal files from the web server. 

The SSH Protocol
~~~~~~~~~~~~~~~~

.. glossary::

    ``clone ssh://[user@]server/.git``
        clone a Git repository over SSH with optional username

Getting Git on a Server
-----------------------

.. glossary::

    ``clone --bare <project_dir> <new-project-dir.git``
         clone and create a new bare repository in new-project-dir.git directory without  a  working  directory

Putting the Bare Repository on a Server
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Generating Your SSH Public Ke
-----------------------------

Setting Up the Server
---------------------

Git Daemon
----------

Smart HTTP
----------

GitWeb
------

GitLab
------

Third Party Hosted Options
--------------------------
