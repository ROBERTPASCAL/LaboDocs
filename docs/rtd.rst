.. _rtd:

Creation de la documentation avec Readthedocs
=============================================

**Créer un compte sur Github et sur Readthedocs.**

------------------------------

**Installer les dépendances :**
::

    [.] sudo apt install python 3.9 python-is-python3 pip3 git
    [.] sudo pip3 install sphinx

------------------------------

**Créer un dossier pour Readthedocs :**
::

    [.] mkdir readthedocs

------------------------------

**Créer un fichier .gitignore :**
::

    [.] cd readthedocs
    [./readthedocs] echo "_*" > .gitignore

------------------------------

**Créer le dossier pour la doc :**
::

    [./readthedocs] mkdir docs

------------------------------

**Executer Sphinx pour créer le template de la doc :**
::

    [./readthedocs] cd docs
    [./readthedocs/docs] sphinx-quickconfig

::

    > Séparer les répertoires build et source (y/n) [n]:
    > Nom du projet: <projet papa>
    > Nom(s) de l'auteur: <John Doe>
    > version du projet []:
    > Langue du projet [en]: fr

------------------------------

**Modifier le fichier conf.py pour changer le template :**
rajouter : import sphinx_rtd_theme

modifier : html_theme = 'alabaster'
par : html_theme = 'sphinx_rtd_theme'

------------------------------

**Créer un dépot <test> dans gitlab**

------------------------------

**Transférer dans le dépot :**
::

    [./readthedocs] git init
    [./readthedocs] git config --global user.name "<John Doe>"
    [./readthedocs] git config --global user.email <johndoe@example.com>
    [./readthedocs] git add *
    [./readthedocs] git commit -m "Creation"
    [./readthedocs] git branch -M main
    [./readthedocs] git remote add origin https://github.com/<ROBERTPASCAL/test.git>
    [./readthedocs] git push -u origin main

------------------------------

**Importer un projet dans Readthedocs**
 * Choisir un nom de projet disponible dans Readthedocs
 * Cocher "Modifier les options avancées du projet"
 * Cliquer sur "Suivant"
 * Selectionner la langue "France"
 * Cliquez sur "Terminer"
 * Une fois le projet créer cliquez sur l'onglet "Admin"
 * Cliquer sur le menu "Paramètres avancés"
 * Selectionnez la "Branche par défaut" de votre projet
 * Cochez "Build pull requests for this project"
 * Cliquez sur "Enregistrer"
 * Cliquez sur "Compiler une version"

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: proxmox
   
   proxmox
