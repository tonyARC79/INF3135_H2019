# Séance 5: Pointeurs, structures, unions, types énumératifs

**Note** : (_facultatif_) S'il y a des questions dans ce labo, répondez y dans un fichier nommé `./labo/reponse-labo.md`.  Le fichier doit être dans un format `Markdown`. Utilisez le projet `inf3135-h2019` pour déposer le fichier `./labo/reponse-labo.md` soit le même que pour vos exercices.  Utilisez un autre `projet` pour vos travaux pratiques.   

##### Format du fichier Markdown
 + Séance 2 (Header 1)
 + Exercice {1..n} (H2)
 + Question {1..n} (H4)
 + S`2`.E`3`.Q`1` (strong) `est une valeur qui change bien sûr`
 + La réponse dans une section script (code block)

**Note**: Il est recommandé de versionner vos réponses aux exercices à l'aide
de Git. Un seul dépôt est amplement suffisant pour tous les laboratoires, en
divisant les fichiers dans des répertoires.

## 1 - Afficher une matrice

Écrivez une fonction C permettant d'afficher le contenu d'une matrice d'entiers
de dimensions 3 par 3.

Rappelons qu'on peut initialiser une matrice de la façon suivante
```c
int matrice[3][3] = { {1, 2, 3}, {4, 5, 6}, {7, 8, 9} };
```
Bien sûr, vous trouverez un moyen d'éliminer les valeurs magiques spécifiant la
taille de la matrice. L'en-tête de votre fonction devrait ressembler à
```c
void afficherMatrice(int matrice[3][3]);
```

Grâce à votre fonction, la matrice sera affichée comme suit:
```
1 2 3
4 5 6
7 8 9
```

## 2 - Addition de matrices

Écrivez une fonction C permettant d'additionner deux matrices.  N'hésitez pas à
réutiliser la fonction de l'exercice précédent pour afficher le résultat.
L'en-tête de votre fonction devrait ressembler à
```c
void additionnerMatrices(int matrice1[3][3],
                         int matrice2[3][3],
                         int resultat[3][3]);
```

Voici un exemple de sortie attendue:

```
1 2 3
3 2 1
1 2 3
+
4 3 2
2 3 4
4 3 2
=
5 5 5
5 5 5
5 5 5
```

## 3 - Structures

Considérez les déclarations suivantes :

```c
struct Point { // Un point en 2D
    double x;  // Sa coordonnée x
    double y;  // Sa coordonnée y
};

struct Segment {
    struct Point p1;
    struct Point p2;
};

struct Triangle {
    struct Point points[3];
};
```

1. Écrivez une fonction
    ```c
    void initialiserSegment(struct Segment *segment, double x1, double y1, double x2, double y2);
    ```
   qui crée un segment dont les extrémités sont les points `(x1,y1)` et `(x2,y2)`.

2. Écrivez une fonction
    ```c
    double longueurSegment(const struct Segment *segment);
    ```
   qui retourne la longueur de `segment`.

3. Écrivez une fonction
    ```c
    void initialiserTriangle(struct Triangle *triangle,
                             double x1, double y1,
                             double x2, double y2,
                             double x3, double y3);
    ```
   qui crée un triangle dont les points sont `(x1,y1)`, `(x2,y2)` et `(x3,y3)`.

4. Écrivez une fonction
    ```c
    double perimetreTriangle(const struct Triangle *triangle);
    ```
   qui retourne le périmètre de `triangle`, c'est-à-dire la somme des longueurs
   de ses côtés. Bien qu'il soit possible de faire le calcul directement,
   faites appel à la fonction `longueurSegment` que vous avez implémentée plus
   tôt.


## 4 - Unions et types énumératifs

Considérons la structure de données suivante :

```c
enum TypeNombre {
    INT, FLOAT, DOUBLE
};

typedef struct {           // Un nombre
    enum TypeNombre type;  // Le type de nombre
    union {
        int i;
        float f;
        double d;
    } valeur;              // La valeur
} Nombre;
```

Donnez l'implémentation d'une fonction dont la signature est
```c
Nombre max(Nombre a, Nombre b);
```
et qui retourne le maximum entre les nombres `a` et `b`, peu importe leur type.

---

## 5 Union (en action) et .h

Vous devez implémenter le code suivant dans un .h et faire un programme qui l'inclura ainsi que répondre aux questions qui suivent: 
~~~~
union L64 {
  unsigned long long n;
  struct {
    unsigned long lo;
    unsigned long hi;
  };
};
~~~~

Une fois le .h fini vous aller écrire un .c qui fera les actions suivantes :
  + mettre une valeur (ex 12345) dans `n`
  + afficher lo et hi
  + mettre une plus grande valeur (ex UULONG_MAX - 10) dans n
  + afficher lo et hi

#### Q1. Que se passe-t-il à la compilation ?
#### Q2. Quelles sont les valeurs de lo et hi (première fois) ?
#### Q3. Quelles sont les valeurs de lo et hi (deuxième fois) ?
#### Q4. Expliquer dans vos mots little endian.
#### Q5. Expliquer dans vos mots big endian (vous pouvez le comparer).

## 6 - Débogueur GDB

Prenez n'importe quel programme dans lequel vous avez une erreur de
segmentation et déboguez-le à l'aide de GDB. Vous pouvez consulter par exemple
le [tutoriel suivant](http://www.unknownroad.com/rtfm/gdbtut/>) comme point de
départ.

---

##### Auteur Guy Francoeur
###### basé sur les travaux d'Alexandre Blondin Massé, Professeur
