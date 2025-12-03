# classGit
## Une petite explication des commandes de base de git

Git est l'outil le plus utiliser pour : 
 - permettre à plusieurs developper de travailler sur sa version 
 - versionner(archiver ou revenor en arrière) notre code, 
 - De fusionner ces codes (branche) de façon à avoir une version complète dans une branche principale(master)
 - avoir une copie en ligne de notre code.

Pour avoir Git :
1. Télécharger git dans le site officiel git-scm.com/download puis l'installer
2. S'inscrire dans github.com pour choisir github comme plateforme de code (y a aussi gitlab, batbucket)
3. Se connecter et accéser à mon repo (les différents projets qu'on crée)
4. On clic sur "new" pour créer un nouveau projet dans mon repo 
5. **gititignore** pour dire à git d'ignorer certains fichiers (des vidoes lourdes par exemple)
6. Choisir la license comme MIT license par exemple puis créer

Pour ajouter un dossier dans **.gititignore**, on ouvre ce dernier avec vsc puis taper **nom_dossier/**

#### Modifiez les Permissions : La solution la plus courante est de s'assurer que 
le propriétaire du fichier (ou tout le monde) dispose des droits de lecture et d'écriture.
 - Méthode 1 : Donner les droits de lecture/écriture au propriétaire (recommandé) : **chmod a+r "mon_fichier**
 - Méthode 2 : Donner les droits de lecture à tout le monde (moins sécurisé, mais efficace) : **chmod a+r "mon_fichier"** 
 
#### Tracker mes fichiers dans dans git
 1. **git clone** <url>	: Copie un projet distant git existant en local
 2. **git status** : Affiche l'état des fichiers (modifiés, stagés, non suivis)
 3. **git add** *mon_fichier* : : Ajoute un fichier à la zone de transit (staging area) 
	**git add .** ou **git add --all **: Ajoute tous les fichiers à la zone de transit
 4. **git commit -m** *"Message"*: Enregistre les modifications de la zone de transit dans le dépôt local.
 5. **git push** : Envoie les commits locaux vers git
 6. **git pull** : Récupère et fusionne les modifications depuis git
 7. **git branch** : Permet de créer, lister ou supprimer des branches.
 8. **git checkout** : Permet de basculer entre les branches.
	ou **git checkout -b** *'dev'* : pour créer une branche *dev*
	**git push --set-upstream origin dev** : pour créer une copie de la branche en ligne.
 9. **git switch** : 
 
 #### Récupèrer des fichoers depuis mon git
  1. **git fetch** : pour avoir le nombre de fichiers qu'on a en local
  2. **git pull** : pour mettre à jour ces fichiers en local

  #### Récuperer une version antérieure
  1. **git log** : Donne l'ensemble des commits avec son message et un **id_commit**
  2. **git checkout** *id_commit* : Permet de changer de version 
  
 Pour de bonne pratique, il est déconseillé de travailler sur la branche principale (main).
 - Créer d'autre à l'aide de **git checkout -b 'new_branch'** et y faire le taf
 - Revenir à la branche **main** (*git branch 'main'*) et fusionner les à l'aide de
  **git merge** *new_branch*
