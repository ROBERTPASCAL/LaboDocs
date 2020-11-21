Creation de la documentation avec Resdthedocs
=============================================
Requirement
-----------
Créer un compte sur Github et sur Readthedocs.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Installer les dépendances :
^^^^^^^^^^^^^^^^^^^^^^^^^^^
::

    [.] sudo apt install python 3.9 python-is-python3 pip3 git
    [.] sudo pip3 install sphinx

Créer un dossier pour Readthedocs :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
::

    [.] mkdir readthedoc

Initialiser Git sur ce dossier :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
::

    [.] cd readthedocd
    [./readthedocs] git init
    [./readthedocs] git config --global user.name "{John Doe}"
    [./readthedocs] git config --global user.email {johndoe@example.com}

.. role:: red 
    This text is :red:`colored red` and so is :red:`this`

.. toctree::
   :maxdepth: 2
   :caption: Contents:

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
