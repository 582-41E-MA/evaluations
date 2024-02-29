# Devoir 1 : Fonctionnement interne de Git

Ce premier devoir vise à évaluer votre compréhension du
fonctionnement interne de Git. Pour ce faire, on vous demande
d'effectuer une série de tâches qui utilisent les commandes de bases
de Git, et d'annoter au fur et à mesure l'état du dépôt.

## Consignes

-   Chaque tâche doit être enregistrée dans un *commit*.
-   Le titre du message de validation doit correspondre à la tâche
    effectuée.
-   Le corps du message doit contenir une description de la base de
    données Git. La description doit inclure le type des objets, les
    cinq premiers caractères de leur empreinte, et ce à quoi ils
    correspondent dans l'arbre de travail.
-   Le message doit respecter le [format prescrit][].

[format prescrit]: https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html

## Astuces

-   La commande `find .git/objects -type f` permet d'afficher tous les
    fichiers du répertoire « .git/objects ».
-   La commande `git cat-file -p <hash>` permet d'afficher le contenu
    de l'objet qui correspond à l'empreinte `<hash>` donné.
-   Pour inclure un message de validation complet (titre et corps),
    exécutez la commande `git commit` sans l'option `-m`.

## Tâches

1.  [Acceptez le devoir][Classroom] et clonez le dépôt sur votre
    ordinateur.
2.  Ajoutez un fichier nommé « NOTES » dont le contenu correspond
    à la sortie de commande de `git log --oneline`.
3.  Ajoutez au fichier `NOTES` la description de la sous-commande
    `status` obtenue à l'aide de `git help`.
4.  Ajoutez un sous-répertoire nommé « resume ».
5.  Dans le sous-répertoire `resume`, ajoutez un fichier nommé
    « objets » qui contient les types d'objets Git.
6.  Toujours dans le fichier `objets`, ajoutez une courte description
    pour chacun des types d'objets.

[Classroom]: https://classroom.github.com/a/4vi_EHlV