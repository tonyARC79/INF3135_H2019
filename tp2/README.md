# Travail pratique 2 modification d'un programme/logiciel

## Objectifs
  L'objectif est de vous initier � la programmation avec le langage C, en  manipulant
  des donn�es, des fichiers, ainsi que la gestion des `arguments` et `options` provenant de la ligne de commande.

  De plus, vos sources seront maintenues dans un gestionnaire de version/source de type git.

  Vous allez aussi vous familiariser avec `make` et le fichier `Makefile` afin `d'automatiser` plusieurs t�ches utiles.

  Dans le `TP2`, nous ajoutons une composante essentielle, les tests. Automatis� des t�ches r�p�titives est quelque chose qui
  reviendra souvent.  Avoir les bons r�flexes et la bonne strat�gie afin de r�soudre un probl�me, vous garantira � coup s�r
  des r�sultats � la hauteur de vos attentes.

## Description du travail

  Le programme doit d�couvrir de nouveaux `nombres parfaits` contenus dans un intervalle compos� d�entiers naturels.
  ```math
   N = { 0, 1, 2, ... }
  ```
  Un nombre est dit parfait lorsque la somme des tous ses diviseurs (excluant lui-m�me bien s�r) est �gal � lui-m�me.

## Qualit� du livrable

### Livrer un logiciel parfait est exig�, nous allons donc mettre un peu plus de temps afin de mieux comprendre et livrer un produit de grande qualit�.

 + toutes les fonctionnalit�s du `TP1` doivent �tre pr�sentes et r�par�es;
 + le fichier `Makefile` doit �tre pr�sent et fonctionnel;
 + le fichier `cp.txt` doit contenir votre code permanent doit �tre pr�sent � la racine de votre projet;
 + aucune librairie non standard; `getopt.h` n'est pas accept�;
 + le fichier `tp2.c` doit contenir uniquement la fonction main();
 + un fichier `outils.h` et un fichier `outils.c` doit exister;
 + tous les fichiers devront �tre dans un format linux.

## Fichier de tests
 + Tous les tests contenus dans le fichier `inf3135-h2019-tp1.correction` doivent �tre ex�cut�s sans probl�me par le script `evaluer.sh`.

## Exigences sp�cifiques
 + toutes les informations ou demandes devront �tre ajout�es au `wiki` et les questions � la section `issues`;
 + aucune question par courriel;
 + toutes les questions devront �tre pos�es dans le gestionnaire de version;
 + vous pouvez guider vos coll�gues avec des r�ponses; maximum 3 interventions (questions ou r�ponses);
 + la qualit� des interventions sera not�e;
 + la qualit� du fran�ais sera aussi not�e;
 + les questions sont pour l'obtention de pr�cision uniquement;
 + si une question vise un �l�ment acad�mique incompris, nous adresserons celui-ci en classe;
 + aucune demande de solution ne sera tol�r�e;
 + aucun manque de respect ne sera tol�r�.

### Vous devez avoir votre propre projet dans votre gestionnaire de version pr�f�r� :
+ le fuseau horaire doit �tre correctement configur� (Montr�al);
+ le nom du projet doit �tre en minuscule et sans faute;
+ les utilisateurs de GitLab doivent s'assurer que la s�curit� soit ad�quate;
+ vous n'avez pas � cr�er de r�pertoire pour ce travail.

# Bar�me de correction

| Crit�re | Sous-crit�re | Points |
| ------- |:------------ | ------:|
| Script (test)     | Script bash pour test `evaluer.sh`               | 2.0 |
| Compilation       | sans avertissement ni erreur                     | 1.0 |
| Fonctionnabilit�  | 5 � 10 tests seront lanc�s (comparaison binaire) | 5.0 |
| Qualit�           | temps d'ex�cution (performance) et code          | 3.0 |
| Makefile          |                                                  | 1.0 |
| Contribution      | wiki et issues                                   | 1.0 |
| Reflexion         | Qualit� des r�ponses                             | 1.0 |
| Fran�ais          | Fran�ais, comprehension                          | 1.0 |
| **Total**         |                                                  |  15 |