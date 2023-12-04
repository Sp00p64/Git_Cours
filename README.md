# Git_Cours

## Présentation de l'outil GIT

### checkout
La commande
``` 
git checkout 
```
Permet plusieurs fonctionnalités notamment: 
- Le changement de branches qui permet de changer de branche active dans le dépôt local. Lorsque cette commande est exécutée, Git met à jour le répertoire pour refléter la dernière révision de la branche choisie, et déplace le HEAD pour pointer sur cette branche. 

    Example:
    ``` 
    git checkout [branche]
    ```

- La création de nouvelles branches, une nouvelle branche sera crée localement et le répéroire sera mis a jour pour se déplacer automatique vers cette nouvelle branche.

    Example:
    ``` 
    git checkout -b [nouvelle-branche]
    ```

- La réstauration de fichier : cette commande peut également être utilisé pour restaurer un fichier à son état lors de la dernière commit cela permet d'annuler les modifications qui n'ont pas été commitées sur un fichier spécifique.

    Example:
    ``` 
    git checkout -- [fichier]
    ```
