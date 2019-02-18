# Travail pratique 2 modification d'un programme/logiciel

## Objectifs
  L'objectif est de vous initier à la programmation avec le langage C, en  manipulant
  des données, des fichiers, ainsi que la gestion des `arguments` et `options` provenant de la ligne de commande.

  De plus, vos sources seront maintenues dans un gestionnaire de version/source de type git.

  Vous allez aussi vous familiariser avec `make` et le fichier `Makefile` afin `d'automatiser` plusieurs tâches utiles.

  Dans le `TP2`, nous ajoutons une composante essentielle, les tests. Automatisé des tâches répétitives est quelque chose qui
  reviendra souvent.  Avoir les bons réflexes et la bonne stratégie afin de résoudre un problème, vous garantira à coup sûr
  des résultats à la hauteur de vos attentes.

## Description du travail

  Le programme doit découvrir de nouveaux `nombres parfaits` contenus dans un intervalle composé d’entiers naturels.
  ```math
   N = { 0, 1, 2, ... }
  ```
  Un nombre est dit parfait lorsque la somme des tous ses diviseurs (excluant lui-même bien sûr) est égal à lui-même.

## Qualité du livrable

### Livrer un logiciel parfait est exigé, nous allons donc mettre un peu plus de temps afin de mieux comprendre et livrer un produit de grande qualité.

 + toutes les fonctionnalités du `TP1` doivent être présentes et réparées;
 + le fichier `Makefile` doit être présent et fonctionnel;
 + le fichier `cp.txt` doit contenir votre code permanent doit être présent à la racine de votre projet;
 + aucune librairie non standard; `getopt.h` n'est pas accepté;
 + le fichier `tp2.c` doit contenir uniquement la fonction main();
 + un fichier `outils.h` et un fichier `outils.c` doit exister;
 + tous les fichiers devront être dans un format linux.

## Fichier de tests
 + Tous les tests contenus dans le fichier `inf3135-h2019-tp1.correction` doivent être exécutés sans problème par le script `evaluer.sh`.

## Exigences spécifiques
 + toutes les informations ou demandes devront être ajoutées au `wiki` et les questions à la section `issues`;
 + aucune question par courriel;
 + toutes les questions devront être posées dans le gestionnaire de version;
 + vous pouvez guider vos collègues avec des réponses; maximum 3 interventions (questions ou réponses);
 + la qualité des interventions sera notée;
 + la qualité du français sera aussi notée;
 + les questions sont pour l'obtention de précision uniquement;
 + si une question vise un élément académique incompris, nous adresserons celui-ci en classe;
 + aucune demande de solution ne sera tolérée;
 + aucun manque de respect ne sera toléré.

### Vous devez avoir votre propre projet dans votre gestionnaire de version préféré :
+ le fuseau horaire doit être correctement configuré (Montréal);
+ le nom du projet doit être en minuscule et sans faute;
+ les utilisateurs de GitLab doivent s'assurer que la sécurité soit adéquate;
+ vous n'avez pas à créer de répertoire pour ce travail.

# Barème de correction

| Critère | Sous-critère | Points |
| ------- |:------------ | ------:|
| Script (test)     | Script bash pour test `evaluer.sh`               | 2.0 |
| Compilation       | sans avertissement ni erreur                     | 1.0 |
| Fonctionnabilité  | 5 à 10 tests seront lancés (comparaison binaire) | 5.0 |
| Qualité           | temps d'exécution (performance) et code          | 3.0 |
| Makefile          |                                                  | 1.0 |
| Contribution      | wiki et issues                                   | 1.0 |
| Reflexion         | Qualité des réponses                             | 1.0 |
| Français          | Français, comprehension                          | 1.0 |
| **Total**         |                                                  |  15 |