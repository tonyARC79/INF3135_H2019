# Q & R TP1

+ Les détails qui suivent s'ajoute à l'énoncé d'origine.

### Q. Le fait d’utiliser le même nom de fichier ou se trouve le main, sommes-nous obligés d’utiliser le fichier .h et faire un include?
#### Réponse 
~~~~
Vous n'êtes pas obligé d'avoir un .h (header) dans ce travail.
~~~~

### Q. Est ce qu’on doit valider le code permanent ou les nombres, et retourner un message d’erreur si non valide ?
#### Réponse
`Attention` *changement de réponse*
~~~~
Suite à plusieurs demandes, je change ma réponse de non à OUI.

Donc, assurez-vous que le code est 12 de long (donc présent). Dans le 
cas contraire, on arrête le programme et un code de retour est émis.

Le code est uniquement nécessaire pour associer le travail à un
individu et publier vos résultats.
~~~~


### Q. Est ce qu’il serait possible qu’il y ait une erreur ou corruption dans le fichier data.zip
#### Réponse
~~~~
Soyez certain de prendre le lien du tp1.md. Il y a le mot 'raw' dans le url.
Il s'agit d'un fichier binaire (zip), il faut le transférer comme tel.
~~~~


### Q. Est-ce que les fichiers pour les tests (./data) ont obligatoirement comme extension .txt ?
#### Réponse
~~~~
Les fichiers sont de type texte, mais pas obligatoirement avec une extension .txt.
~~~~


### Q. Devons nous faire les tests de temps d’exécutions en termes de valeur de temps ?
#### Réponse
~~~~
C'est une bonne chose en général.  Le temps réponse sera sûrement évalué.
~~~~

### Q.  La commande make test lance le logiciel avec quelle commande? Doit-on lancer le logiciel 2 fois pour tester les deux commandes? Doit-on lancer et/ou exécuter d'autres tests?
#### Réponse
~~~~
pour make test : Une fois, à votre choix, les tests sont pour vous. (c'est le minimum exigé)

Si vous avez besoin de plusieurs tests (ex pour faire les autres commandes) vous avez toujours
le loisir de créer un test2, test3, test4 ou test_all.  
Faire ce qui vous rend confortable. Des tests il y en a jamais trop!
~~~~
### Q. Allez-vous nous fournir une série de tests pour l'évaluation? Sinon, doit-on la créer nous-mêmes?
#### Réponse
~~~~
data.zip
~~~~

### Q. Faut-il faire la documentation? J'ai l'habitude de la faire par défaut, mais est-ce qu'il y a des exigences par rapport au TP1?
#### Réponse
~~~~
Le fichier .md sera votre documentation. Si vous en faites plus que demander aucun problème.
~~~~

### Q. Peut-on modifier la structure établie? J'ai été habitué à utiliser un dossier src et bin, alors je me demandais si je pouvais configurer mon TP1 ainsi?
#### Réponse
~~~~
Pas pour ce travail. Le prochain peut-être.
~~~~

### Q. La session passée j'ai perdu 15% parce que je n’avais pas mis suffisamment de couleur dans l'un de mes README.md, donc je voudrais savoir s'il est nécessaire d'être ultra fancy sur le README.md dans le cadre de ce TP1?
#### Réponse
~~~~
Wow, OK.. Suivre les instructions du TP le plus possible.  La simplicité est sûrement la meilleure
piste pour réaliser le travail.  Tout va bien aller. Consultez le barème de correction.
~~~~

### Q. Doit-on ajouter une licence au projet ?
#### Réponse
~~~~
Ce n'est pas demandé.
~~~~

### Q. Est-ce qu'on devrait vérifier que le contenu du fichier d'entrée est valide?
#### Réponse
~~~~
Oui, on ne sait jamais ce qu'il pourrait contenir.  Une corruption de fichier pourrait survenir.
~~~~

### Q. Est ce qu'un fichier d'entrée valide peut contenir plusieurs intervalles dans lesquels on doit chercher les nombres parfaits ? ou il doit juste contenir un seul intervalle sans aucun texte autour ?
#### Réponse
~~~~
Un seul intervalle
~~~~

### Q. Que fait-on lorsqu'il y a des erreurs ou que quelque chose n'est pas pas conforme ?
#### Réponse
~~~~
Toutes les applications lorsqu'elles rencontrent un problème avec les données, les arguments ou autres
influences qui empêchent un fonctionnement conforme retournent un code.
C'est le cas pour les applications ou les commandes Linux (ie.: cd, cat, ls, sed, gcc, ... ) qui sont 
basés sur ce principe. Donc, vous devez les gérer les codes de retour.  Pour vous aidez et vous guider,
voici la liste des codes de retour que votre application doit supporter :
~~~~
#### Détails sur les codes de retour
+ `0` : le programme s’est exécuté avec succès;
+ `1` : il n'y a `aucun` d'argument ou l'argument `-c` n'est pas présent;
+ `2` : l'argument -c est présent, mais le code n'est pas 12 de long;
+ `3` : un argument non voulu est présent. Voici un exemple : `-t BLA`;
+ `4` : l'intervalle n'est pas conforme; 
+ `5` : une erreur (lecture, existance, ...) avec le fichier en entrée;
+ `6` : une erreur (création, ...) avec le fichier en sortie; `Attention` Si le fichier existe il faut l'écraser;

#### Pour les codes `0`, `2`, `3`, `4`, `5`, `6` 
 + Aucun message n'est nécessaire. Le code de retour est suffisant.

#### Pour le code `1` uniquement
 + Il semble judicieux d'informer l'utilisateur que votre application a certains requis: 
~~~~ 
 fprintf(stderr, "Usage: %s <-c CODEpermanent> [-i fichier.in] [-o fichier.out] \n", argv[0]);
~~~~
#### Pour le code `4` voici des précisions
+ un intervalle `1000 0` est valide.
+ L'ensemble valide est : N = entiers naturels; qui inclu 0;
