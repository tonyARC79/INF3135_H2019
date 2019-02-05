# Séance 6: 

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

## 1 - Implémentation d'une file

Complétez l'implémentation d'une structure de données de type "file" (en
anglais *queue*) à partir des déclarations suivantes:

```c
// Types
// -----

struct QueueNode {
    char content;           // Contenu du noeud
    struct QueueNode *prev; // Noeud precedent
    struct QueueNode *next; // Noeud suivant
};

typedef struct {
    struct QueueNode *first; // Pointeur vers le premier noeud
    struct QueueNode *last;  // Pointeur vers le dernier noeud
} Queue;

// Prototypes
// ----------

Queue queueCreate();
bool queueIsEmpty(const Queue *s);
void queuePush(Queue *s, char content);
char queuePop(Queue *s);
void queueDelete(Queue *s);
```

Assurez-vous de gérer correctement la mémoire (pas de fuite)!
