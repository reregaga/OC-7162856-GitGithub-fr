[Quiz](https://openclassrooms.com/en/courses/7162856-gerez-du-code-avec-git-et-github/exercises/4059)
# Corriger les erreurs courantes

## Question 1
**Je suis sur ma Branch1 et je viens d’ajouter un fichier "File2.txt".Je change d’avis : je veux finalement ajouter mon fichier à une nouvelle branche, "BranchFile". Que dois-je faire ?**
- [ ] git statusgit branch BranchFilegit checkout BranchFilegit status apply
- [ ] git statusgit stashgit branch BranchFilegit checkout BranchFilegit status apply
- [x] git statusgit stashgit branch BranchFilegit checkout BranchFilegit stash apply

_Nous abordons ici la remise. Nous allons devoir remiser les changements faits sur Branch1 pour les appliquer ensuite sur la nouvelle branche, "BranchFile".  git stash  permet de remiser des modifications et  git stash apply  permet d'appliquer une remise sur une branche. Vous allez devoir remiser vos modifications de la branch1 à la branchFile en utilisant plusieurs commandes dans un ordre précis : 
- git status pour vérifier l’état de vos fichier
- git stash pour remiser vos modifications
- git branch branchFile pour créer une nouvelle branche
- git checkout BranchFile pour basculer sur cette branche
- git stash apply pour appliquer les modifications_

## Question 2
**git commit --amend -m "Test"
Cette commande permet de :**
- [ ] revenir au commit précédent
- [x] modifier le message du commit précédent
- [ ] créer un nouveau commit avec le message "Test"

_git commit --amend -m  modifie le message du commit précédent. C'est le -m qui indique que nous allons modifier le message._

## Question 3
**Je souhaite revenir sur le commit précédent et modifier son contenu en ajoutant un fichier, que dois-je faire ?**
- [ ] git commit --amend --no editgit add monFichierOubliégit commit
- [x] git add monFichierOubliégit commit --amend --no-edit
- [ ] git commit --amendgit add monFichierOubliégit commit
- [ ] git add monFichierOubliégit commit --amend

_git add monFichierOublié  permet d'ajouter mon fichier.
git commit --amend --no-edit permet de modifier le commit sans changer le message._

## Question 4
**La commande git reset peut être appliquée de 3 façons différentes. Lesquelles ?**
- [x] Git reset --soft  /  Git reset --mixed  /  Git reset --hard
- [ ] Git reset --down  /  Git reset --middle  /  Git reset --up
- [ ] Git reset --safe  /  Git reset --regular  /  Git reset --risky
- [ ] Git reset n’existe pas.

_git reset  peut être appelée de 3 façons différentes, qui correspondent aux arguments de ligne de commande --soft, --mixed et --hard._

## Question 5
**Quelle est la différence entre  git revert  et  git reset  ?**
- [ ] git revert  ne réinitialise qu'un commit alors que  git reset  réinitialise tout.
- [x] git revert  crée un nouveau commit alors que  git reset  , non.
- [ ] git reset  crée un nouveau commit alors que  git revert  , non.

_git reset  ne crée jamais un nouveau commit alors que  git revert  , oui._

## Question 6
**Je souhaite savoir qui a touché à une ligne en particulier dans le fichier test.html. Quelle commande vais-je devoir exécuter ?**
- [ ] git log
- [ ] git reflog
- [x] git blame
- [ ] git cherry pick

_Seule la commande  git blame  permet d’examiner le contenu d’un fichier ligne par ligne et de déterminer la date à laquelle chaque ligne a été modifiée, et le nom de l’auteur des modifications ._

## Question 7
**Vous avez deux branches dans votre projet : branch1 et branch2. Sur branch1, dans le fichier “monfichier”, ligne 10, nous avons “titre”. Sur branch2, dans le fichier “monfichier”, ligne 10, nous avons “titre !”.
Vous avez voulu fusionner ces deux branches et cela a provoqué un conflit. Que devez-vous faire ?**
- [x] Résoudre ce conflit
- [ ] Forcer la fusion
- [ ] Supprimer une branche
- [ ] Demander à Git de faire un choix

_Dans cette situation, il faut résoudre le conflit. Nous avons 2 versions différentes pour la même ligne de code, la seule solution possible est donc de faire un choix et de décider laquelle garder._

## Question 8
**Qu'est ce qu'un SHA ?**
- [ ] Un SHA est un numéro aléatoire permettant de se connecter à GitHub
- [x] Un SHA est un identifiant pour les commits et autres actions gardés en mémoire par Git
- [ ] Un SHA est un petit animal qui ronronne

_Le SHA, c'est ce grand code qui vous permettra de revenir à un commit exact. C'est l’identifiant de votre action !_