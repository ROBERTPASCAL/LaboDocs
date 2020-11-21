.. laboDocs documentation master file, created by
   sphinx-quickstart on Sat Nov 21 16:01:36 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Creation de la documentation avec Readthedocs
=============================================
Requirement
-----------
Créer un compte sur Github et sur Readthedocs.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Installer les dépendances :
"""""""""""""""""""""""""""
::

    [.] sudo apt install python 3.9 python-is-python3 pip3 git
    [.] sudo pip3 install sphinx

Créer un dossier pour Readthedocs :
"""""""""""""""""""""""""""""""""""
::

    [.] mkdir readthedocs

Initialiser Git sur ce dossier :
""""""""""""""""""""""""""""""""
::

    [.] cd readthedocs
    [./readthedocs] git init
    [./readthedocs] git config --global user.name "{John Doe}"
    [./readthedocs] git config --global user.email {johndoe@example.com}

créer un fichier .gitignore :
"""""""""""""""""""""""""""""
::

    [./readthedocs] echo -e "_*\nmake.bat\nMakefile" > .gitignore

Créer le dossier pour la doc :
""""""""""""""""""""""""""""""
::

    [./readthedocs] mkdir docs
    
Executer Sphinx pour créer le template de la doc :
""""""""""""""""""""""""""""""""""""""""""""""""""
::

    [./readthedocs] cd docs
    [./readthedocs/docs] sphinx-quickconfig
 
::

    > Séparer les répertoires build et source (y/n) [n]: 
    > Nom du projet: <projet papa>
    > Nom(s) de l'auteur: <John Doe>
    > version du projet []: 
    > Langue du projet [en]: fr

Modifier le fichier conf.py pour changer le template :
""""""""""""""""""""""""""""""""""""""""""""""""""""""
rajouter : import sphinx_rtd_theme

modifier : html_theme = 'alabaster'
par : html_theme = 'sphinx_rtd_theme'

faire un commit des fichiers :
""""""""""""""""""""""""""""""
::

    git add .gitignore
    git add *
    git commit -m "Creation"


.. toctree::
   :maxdepth: 2
   :caption: Contents:

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
