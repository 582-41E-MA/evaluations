# Devoir 2 : Git intermédiaire

![Caricature de messages Git](git_commit.png)

Ce deuxième devoir vise à évaluer votre maîtrise de l'utilisation locale
de Git. Pour ce faire, on vous demande d'effectuer une série de tâches,
et de prendre en note le graphe du dépôt au fur des changements.

## Consignes

-   Chaque tâche doit être enregistrée dans un *commit*.
-   Le titre du message de validation doit correspondre à la tâche
    effectuée.
-   Le corps du message doit contenir le graphe du dépôt au moment du
    commit (le graphe n'inclura pas ledit *commit* ; c'est normal).
    Pour obtenir le graphe, vous pouvez utiliser la commande `git log
    --all --graph --oneline`.
-   Le message doit respecter le [format prescrit][].

[format prescrit]: https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html

## Astuces

-   La commande `chmod +x <fichier>` permet de modifier la permission
    du `<fichier>` donné afin qu'il puisse être exécuté.
-   Pour exécuter un script shell, préfixez le chemin du fichier par
    `./`. Par exemple, `./greet.sh`.
-   Dans un script shell, `else if` s'écrit `elif`.

## Tâches

-   Créez une nouvelle branches nommée « devoir2 », et basculer vers
    celle-ci. Créez un script shell nommé « greet.sh » dont le contenu
    est le suivant :

    ```sh
    echo "Bonjour"
    ```

-   Créez une nouvelle branche nommée « japonais », et basculer vers
    celle-ci. Ajoutez le contenu suivant au script « greet.sh » :

    ```sh
    if [ "$1" == "japonais" ]; then
        echo "こんにちは"
    else
        echo "Bonjour"
    fi
    ```

-   Sur une autre branche, modifiez le script afin qu'il puisse
    dire « Bonjour » dans une troisième langue.

-   Fusionnez la branche `japonais` dans la branche `devoir2`.

-   Re-baser la branche qui contient les modifications pour le
    troisième langage sur le commit le plus récent de la
    branche `devoir2`, et fusionner les deux branches.