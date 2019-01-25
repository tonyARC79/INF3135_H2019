# Séance 3: Chaînes de caractères, pointeurs et matrices

**Note**: Il est recommandé de versionner vos réponses aux exercices à l'aide
de Git (un seul dépôt est amplement suffisant pour la séance, ou même un seul
dépôt pour tous les laboratoires, en divisant les fichiers dans des
répertoires).

## 1 - Chaînes de caractères

Écrivez un petit programme C appelé `renverse.c` qui prend tous les arguments
passés en paramètres, les concatène en ordre inverse et affiche le résultat.

On s'attend donc au comportement suivant :

```sh
./renverse alpha beta gamma delta
deltagammabetaalpha

./renverse esope reste et se repose
reposeseetresteesope
```

N'hésitez pas à utiliser la bibliothèque `string.h`.

## 2 - Palindromes

Écrivez une fonction C dont la signature est
```c
bool estPalindrome(const char *s);
```
qui retourne `true` si et seulement si `s` est un palindrome, c'est-à-dire un
mot qui se lit de la même façon de gauche à droite. On s'attend donc à ce que
```c
estPalindrome("radar")
estPalindrome("ici")
estPalindrome("laval")
estPalindrome("!RessasseR!")
estPalindrome("")
estPalindrome("U")
```
retournent `true`, mais que
```c
estPalindrome("Lui")
estPalindrome("Ici")
estPalindrome("laval.")
estPalindrome("Esope reste et se repose.")
```
retournent `false`.

Ensuite, écrivez une fonction C dont la signature est
```c
bool estPhrasePalindrome(const char *s);
```
qui vérifie si une phrase est palindromique, en ignorant la casse
(majuscules/minuscules) et les signes de ponctuation. Ainsi, on s'attend à ce
que
```c
estPhrasePalindrome("Esope reste et se repose.")
estPalindrome("Ici")
```
retournent `true`.

Dans les deux cas, fournissez des tests pour montrer que vos fonctions sont
correctement implémentées.

## 3 - Fouille dans un tableau

Écrivez une fonction C dont la signature est
```c
const double *trouverElement(const double tableau[],
                       unsigned int taille,
                       double element);
```
qui retourne un pointeur vers la première occurrence de `element` dans
`tableau` si elle existe, ou qui retourne `NULL` sinon, sachant que les indices
valides de `tableau` sont entre `0` et `taille - 1`.

---

##### Auteur Guy Francoeur
###### basé sur les travaux d'Alexandre Blondin Massé, Professeur
