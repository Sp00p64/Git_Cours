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

### PULL
La commande
``` 
git pull
``` 
Permet de :
- La commande git pull est un outil essentiel dans la gestion de versions collaboratives lors du développement de logiciels. Elle permet de récupérer les dernières modifications d'un dépôt distant vers votre copie locale du projet.

<ins>I. Contexte :

- Développement collaboratif : Dans un environnement de développement collaboratif, plusieurs contributeurs travaillent simultanément sur un même projet.

- Système de contrôle de versions : Git est un système de contrôle de versions largement utilisé qui permet de gérer ces modifications en enregistrant les différentes versions du code.

<ins>II. Composants :

- Dépôt local : Votre copie du projet sur votre ordinateur.
Dépôt distant : Un référentiel centralisé, comme GitHub ou GitLab, où d'autres contributeurs publient leurs modifications.

<ins>III. Fonctionnement de git pull :

Récupération des modifications : La commande git pull combine deux actions en une :

- Récupère les dernières modifications du dépôt distant sans les fusionner avec votre code actuel.
- Fusionne les modifications récupérées avec votre code local.
Mise à jour du code local : Après l'exécution de git pull, votre copie locale est synchronisée avec les dernières modifications du dépôt distant.

<ins>IV. Utilisation :

Syntaxe de base : 
``` 
git pull <dépôt distant> <branche>
``` 
<ins>Exemple</ins> : Supposez que vous travailliez sur la branche "master" et souhaitez récupérer les modifications du dépôt distant appelé "origin" :

``` 
git pull origin master
``` 
<ins>V. Précautions :

<ins>Conflits</ins> : Des conflits peuvent survenir si les mêmes parties du code ont été modifiées à la fois localement et à distance. Dans de tels cas, une résolution manuelle des conflits est nécessaire.

<ins>Branches multiples</ins> : Lors de l'utilisation de branches multiples, assurez-vous de spécifier la branche à tirer (pull) depuis le dépôt distant.