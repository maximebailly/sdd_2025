# UE 21.2 EC Science des données
Cours « science des données » à Mines Paris (2025). [![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-sa/4.0/)

__Organisation de ce repo__
* `environment.yml` permet de charger l'environnement conda pour les notebooks via l'interface graphique d'Anaconda ou 
```bash
   conda env create -f environment.yml -n sdd2025
   conda activate sdd2025
```

(Vous pouvez aussi utiliser `mamba` plutôt que `conda`, `mamba` est plus rapide et s'installe via `conda install mamba`.)

Notez que cet environnement vous fait utiliser JupyterLab et non pas Jupyter Notebook. JupyterLab est plus moderne et plus agréable d'utilisation (voir [la documentation](https://jupyterlab.readthedocs.io/en/stable/)). En particulier, JupyterLab permet de copier des cellules entre notebooks, et l'[extension "Table of contents"](https://github.com/jupyterlab/jupyterlab-toc/blob/master/toc.gif) qui facilite la navigation dans un notebook y est native.
* `poly/` contient tous les fichiers permettant de compiler le poly. La dernière version compilée à jour s'intitule `sdd_2025_poly.pdf`
* `pc/` contient un répertoire par PC
* `projet/` contient les données et instructions relatives au projet numérique

__Équipe pédagogique__
* Responsables de cours : Chloé-Agathe Azencott et Émilie Chautru
* Chargé·e·s d'enseignement : Valentin Alleaume, Katia Antonenko, Antoine Bottenmuller, Julie Cartier, Théo Dumont, Paul Etheimer, Thibault Faney, Daniel Mimouni, et Marie Verbanck.

__Emploi du temps__
* __lundi 2/06 :__ 
  * __13h45-15h15 :__ amphi 1 — Introduction et statistique descriptive (Chapitres 1 & 2)
  * __15h30-17h00 :__ amphi 2 — Techniques d'estimation (Chapitre 3)

* __vendredi 6/06 :__
  * __13h45-15h15 :__ PC 1 — Estimation (TD)
  * __15h30-17h00 :__ amphi 3 — Tests statistiques (Chapitre 4)

* __vendredi 13/06 :__
  * __13h45-15h15 :__ PC 2 — Test statistiques (TD)
  * __15h30-17h00 :__ amphi 4 — Réduction de dimension (Chapitre 5)

* __lundi 16/06 :__
  * __13h45-15h15 :__ PC 3 — Réduction de dimension (TP)
  * __15h30-17h00 :__ amphi 5 — Introduction à l'apprentissage supervisé (Chapitre 7)

* __vendredi 20/06 :__
  * __13h45-15h15 :__ Mini-projet numérique (1)
  * __15h30-17h00 :__ amphi 6 — Bonnes pratiques (Chapitre 6)

* __lundi 23/06 :__
  * __13h45-15h15 :__ PC 4 — Pré-traitement & introduction à scikit-learn pour l'apprentissage supervisé (TP)
  * __15h30-17h00 :__ amphi 7 — Généralisation (Chapitre 8)

* __vendredi 27/06 :__
  * __13h45-15h15 :__ PC 5 — Sélection de modèles (TP)
  * __15h30-17h00 :__ amphi 8 — Modèles d'apprentissage supervisé non-linéaires (Chapitre 9) 

* __lundi 7/07 :__
  * __13h45-15h15 :__ PC 6 — Modèles linéaires pour la classification (TD)
  * __15h30-17h00 :__ Mini-projet numérique (2)

* __jeudi 10/07 13h45-17h : examen écrit et rendu de projet numérique.__

__Modalités d'évaluation__
* mini-projet numérique à réaliser en binôme. Deux séances de PC y sont dévouées (le 20/06 et le 7/07). À rendre le 10/07 (30%).
* examen sur table avec documents autorisés le 10/07 (70%).

__Pour contribuer à ce repo__
Ce repo contient un script `pre-commit.sh` qui permet de le nettoyer (supprimer les fichiers auxiliaires de latex, nettoyer les notebooks avec [`nbstripout`](https://pypi.org/project/nbstripout/)).

Il est possible de lancer automatiquement ce script lors d'un `git commit` grâce à un [`hook`](https://githooks.com/). Pour cela, il suffit de le copier dans le fichier `.git/hooks/pre-commit` ou d'utiliser un lien symbolique (pour conserver le contrôle de version) :
```bash
    cd .git/hooks/
    ln -s ../../pre-commit.sh pre-commit
```
