[Quiz](https://openclassrooms.com/en/courses/7162856-gerez-du-code-avec-git-et-github/exercises/4058)
# Utiliser les commandes de base de Git

## Question 1
**Quelles sont les trois zones locales majeures dans Git ?**
- [x] Working directory
- [ ] Cloud
- [x] Repository
- [x] Index

_3 zones locales majeures

Git gère les versions de vos travaux locaux à travers 3 zones locales majeures :

le répertoire de travail (working directory/WD) ;
l’index ou stage ;
le dépôt local (Git directory/repository).

Le répertoire de travail désigne l'arborescence de vos fichiers, c'est-à-dire tous vos fichiers et répertoires qui sont indépendants de Git. Ils sont même là avant que vous réalisiez votre git init !L'index ou stage désigne tous les fichiers modifiés que vous souhaitez voir apparaître dans votre prochain commit. C'est avec la commande  git add  que l'on ajoute un fichier à l’index. Le dépôt local est l'historique de l'ensemble de vos actions (commits, configurations...)._

## Question 2
**Vous avez créé votre dépôt distant sur GitHub, que l'on appellera monDepotDistant, et vous souhaitez maintenant le lier avec votre dépôt local sur Git. DEP représente le nom court qui sera utilisé pour appeler le dépôt.Quelle ligne de commande devez-vous taper ?**
- [ ] git remote DEP https://github.com/xxxxxx/monDepotDistant
- [ ] git remote DEP add https://github.com/xxxxxx/monDepotDistant
- [x] git remote add DEP https://github.com/xxxxxx/monDepotDistant
- [ ] git add DEP https://github.com/xxxxxx/monDepotDistant

_Pour lier votre dépôt local au dépôt distant, vous devez effectuer la commande :
git remote add DEP https://github.com/xxxxxx/monDepotDistant
La commande git remote doit être effectuée sous la forme : git remote add leNomCourt "URL de votre dépôt".
Les autres commandes ne sont pas valides._

## Question 3
**Maintenant que votre dépôt distant est lié à votre dépôt local, vous allez devoir dupliquer son contenu en local. Pour ce faire, nous devons utiliser :**
- [ ] git clone DEP https://github.com/xxxxxx/monDepotDistant
- [ ] git duplicate https://github.com/xxxxxx/monDepotDistant
- [x] git clone https://github.com/xxxxxx/monDepotDistant
- [ ] git duplicate DEP

_La commande git clone permet de dupliquer le contenu distant en local. Pour être valide, cette commande doit être écrite sous la forme : git clone https://github.com/nom-dutilisateur/monDossier.  La commande git duplicate n’existe pas._

## Question 4
**Nous allons désormais ajouter des branches à notre dépôt. Je souhaite créer trois nouvelles branches : "Branch1", "Branch2" et "Branch3", et basculer sur ma branche "Branch2". Que dois-je faire ?**
- [ ] git branchgit branchgit branchgit checkout branch
- [x] git branch Branch1git branch Branch2git branch Branch3git checkout Branch2
- [ ] git checkout Branch1git checkout Branch2git checkout Branch3git branch

_Pour créer chacune des branches, vous devez utiliser la commande git branch, puis réaliser un git checkout sur la branche où vous souhaitez basculer. Utilisée seule, la commande git branch permet de visualiser les différentes branches d’un projet._

## Question 5
**Quelle commande permet de consulter nos branches, et quel est le résultat de cette commande ?**
- [x] git branchmainBranch1*Branch2Branch3
- [ ] git checkoutmainBranch1*Branch2Branch3
- [ ] git branchBranch1*Branch2Branch3
- [ ] git checkoutBranch1*Branch2Branch3

_La commande git branch permet de consulter l'état de notre arbre, et ici de visualiser 4 branches : Branch1, Branch2, Branch3 et notre branche principale, la branche “main”. La commande git checkout permet de basculer d'une branche à une autre._

## Question 6
**Vous devez maintenant réaliser des modifications sur votre branche Branch2, puis créer une version en indiquant le message "Je suis le roi du commit". Comment faites-vous cela ?**
- [ ] git commit "Je suis le roi du commit"
- [x] git commit -m “Je suis le roi du commit”
- [ ] git commit -m -n “Je suis le roi du commit”
- [ ] commit

_git commit -m permet de réaliser un commit en indiquant un message de description. Les autres commandes ne sont pas valides._

## Question 7
**Dans quel ordre dois-je réaliser les 3 commandes ?**
- [x] git add fichier.htmlgit commit -m “message”git push origin main
- [ ] git add fichier.htmlgit push origin maingit commit -m “message”
- [ ] git push origin maingit add fichier.htmlgit commit -m “message”
- [ ] git commit -m “message”git add fichier.htmlgit push origin main

_Pour commencer, on indexe le fichier .html avec la commande  git add  , puis on crée une version avec la commande  git commit  , et enfin on envoie cette version sur le dépôt distant avec la commande  git push origin main  . Les autres commandes ne sont pas valides._

## Question 8
**Je veux fusionner la branche “modifications” à la branche principale du projet. Quelles commandes dois-je réaliser ?**
- [x] git checkout maingit merge modifications
- [ ] git checkout modificationsgit merge main
- [ ] git merge modificationsgit checkout main
- [ ] git merge maingit checkout modifications

_La commande merge doit s'utiliser à partir de la branche dans laquelle nous voulons apporter les évolutions. Nous voulons apporter les évolutions de la branche “modifications” dans la branche principale (main). Nous devrons donc utiliser les commandes :
git checkout maingit merge modifications_