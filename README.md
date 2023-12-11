# Git_Cours

## Présentation de l'outil GIT
GIT est un système de contrôle de version décentralisé, utilisé principalement pour la gestion du code source dans le développement de logiciels. 
## git init

La commande git init crée un nouveau dépôt Git dans le répertoire courant. Elle crée un fichier .git qui contient les informations de configuration du dépôt, notamment la branche courante, les commits et les branches distantes.

## git add

La commande git add ajoute les modifications apportées aux fichiers à l'index Git. L'index est une zone de stockage temporaire qui contient les modifications que vous souhaitez valider.

Pour ajouter tous les fichiers qui ont été modifiés ou créés, utilisez la commande suivante :

"git add ."

Pour ajouter un fichier spécifique, utilisez la commande suivante :

"git add <fichier>"

## git commit

La commande git commit enregistre les modifications de l'index dans un commit. Un commit est une unité de base de la gestion de versions Git. Il contient les modifications apportées aux fichiers, la date et l'heure du commit, ainsi un message qui décrit les modifications apportées.

Pour créer un commit, utilisez la commande suivante :

git commit -m "message du commit"

### PULL
La commande
``` 
git pull
``` 
Permet de :
- La commande **git pull** est un outil essentiel dans la gestion de versions collaboratives lors du développement de logiciels. Elle permet de récupérer les dernières modifications d'un dépôt distant vers votre copie locale du projet.

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

### Diff

La commande **git diff** est un outil essentiel pour examiner les différences entre les différentes versions des fichiers dans un projet. Elle permet de visualiser les changements apportés au code entre deux états distincts.

<ins>I. Contexte :</ins>

Analyse des modifications : Dans le développement logiciel, il est crucial de comprendre les changements apportés au code source pour suivre l'évolution du projet.

<ins>II. Fonctionnement de git diff :</ins>

- Comparaison des versions : La commande git diff compare deux états du code pour montrer les différences entre eux.

- États de comparaison : Vous pouvez comparer différents états tels que :

- Différences entre commits : Compare les modifications entre deux points spécifiques de l'historique du projet.
Différences de fichiers non suivis : Montre les modifications apportées à des fichiers qui ne sont pas encore ajoutés au suivi de version.
Affichage des changements : git diff affiche les lignes ajoutées, supprimées ou modifiées entre les deux états comparés.

<ins>III. Utilisation :</ins>

Syntaxe de base :
``` 
 git diff <source> <cible>
``` 
<ins>Exemple :</ins> Pour voir les différences entre le dernier commit et l'état actuel du répertoire de travail :

``` 
git diff HEAD
``` 
<ins>IV. Informations supplémentaires :</ins>

Options supplémentaires : git diff offre diverses options pour personnaliser la sortie, comme limiter la portée de la différence à un fichier spécifique ou à un répertoire.

Visualisation claire : Les modifications sont affichées de manière intuitive avec des symboles comme '+' pour les ajouts et '-' pour les suppressions.

<ins>V. Importance :</ins>

- Analyse des changements : Permet de comprendre les modifications apportées au code, ce qui est crucial pour suivre le développement d'un projet et pour débugger des problèmes.

- Préparation des commits : Aide à examiner les modifications avant de les inclure dans un commit, assurant ainsi la qualité et la cohérence du code.

### TAG

La commande **tag** dans le contexte du développement logiciel est utilisée pour marquer des points spécifiques dans l'historique des versions d'un projet. Ces points marqués, appelés "tags", permettent de référencer des versions spécifiques du code pour les identifier facilement ultérieurement.

<ins>I. Signification des "tags" :

Marquer des versions : Les "tags" sont des étiquettes assignées à des commits particuliers, représentant des versions stables, des versions majeures, des jalons ou des versions spécifiques du code.

<ins>II. Fonctionnement de la commande tag :

Création de tags :

- Annotés : Ces tags sont des versions spécifiques associées à un message pour une identification claire et sont créés à l'aide de la commande 
``` 
git tag -a <nom_tag> -m "Message descriptif" <commit_hash>
``` 
- Légers : Ces tags sont des références simples à un commit particulier et sont créés avec la commande 
``` 
git tag <nom_tag> <commit_hash>
``` 
- Liste et affichage des tags : La commande **git tag** permet d'afficher tous les tags existants dans le dépôt.

<ins>III. Utilisation :

Création d'un tag : Pour créer un tag annoté avec un message associé :

``` 
git tag -a v1.0 -m "Version 1.0" <commit_hash>
``` 
Lister les tags : Pour afficher tous les tags existants :
``` 
git tag
``` 
<ins>IV. Importance des "tags" :

Repères pour les versions stables : Ils offrent des repères clairs pour identifier des versions spécifiques du code qui sont stables et peuvent être référencées facilement.

Facilite la gestion des versions : Les "tags" simplifient la gestion des versions en permettant aux développeurs de revenir facilement à des versions précédentes du code si nécessaire.
main

## `git clone`

La commande `git clone` permet de copier un dépôt Git existant dans un nouveau répertoire, sur votre ordinateur.

### Syntaxe de base

```bash
git clone <url-du-dépôt>
```

- `<url-du-dépôt>` : l'URL du dépôt Git que vous souhaitez cloner.

### Exemple d'utilisation

```bash
git clone https://github.com/exemple/mondepot.git
```

Cette commande va cloner le dépôt situé à `https://github.com/exemple/mondepot.git` dans un dossier `mondepot` sur votre ordinateur.

## Options courantes

- `--branch <nom-de-branche>` : Permet de cloner une branche spécifique.
- `--depth <profondeur>` : Crée un clone superficiel avec un historique à la profondeur spécifiée.

### Exemple avec options

```bash
git clone --branch ma-branche https://github.com/exemple/mondepot.git
```

Cette commande clone seulement la branche `ma-branche` du dépôt.

## Bonnes pratiques

- Vérifiez toujours que vous clonez le bon dépôt.
- Utilisez des clones avec depth (`--depth`) pour de gros dépôts afin d'économiser de l'espace disque et du temps.

## Conclusion

La commande `git clone` permet de copier facilement tout le contenu d'un dépôt distant vers votre espace de travail.

<br>

## Commande `git stash`

## Introduction

`git stash` est une commande Git qui permet de mettre de côté des modifications temporaires, afin de pouvoir travailler sur autre chose sans "commit" ces changements.


### Mettre des changements en attente

```bash
git stash
```

Cette commande met en attente les modifications non commitées.

### Appliquer des changements mis en attente

```bash
git stash pop
```

Cela réapplique les modifications les plus récentes mises en attente.

## Options courantes

- `git stash list` : Affiche la liste des stashs.
- `git stash drop` : Supprime le stash le plus récent.

## Bonnes pratiques

- Utilisez `git stash` pour éviter des commits précipités.
- Gardez une trace de ce que chaque stash contient pour éviter la confusion.

## Conclusion

`git stash` est un outil utile pour gérer temporairement des modifications sans perturber le flux de travail principal.

### Commande `checkout`
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
