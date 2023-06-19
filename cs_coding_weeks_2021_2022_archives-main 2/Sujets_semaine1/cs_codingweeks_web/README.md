# Développement d'applications web en Django



## Bienvenue aux Coding Weeks !
### Cet espace correspond au projet **Développement d'applications web en Django** de la première semaine des coding weeks.

Ce séminaire de deux semaines va vous permettre de monter en compétences en développement et développement web (utilisation de Git, Gitlab, python, Django, etc). A l'issue de cette période, vous serez en mesure de créer un petit site web fonctionnel.

Ce cours sera divisé en deux séquences. La première semaine sera dédiée à l'apprentissage. La seconde sera une semaine projet où vous développerez une application web de votre choix.
## Prérequis

### Rejoindre les espaces de l'activité

Avant de commencer, merci de bien vouloir :

- rejoindre l'équipe TEAMS de code **ucn55jj** 

- vous répartir par équipe de cinq et de noter votre équipe sur cet [classeur](https://centralesupelec.sharepoint.com/:x:/s/CS_Coding_Weeks_prog_Web/EZiEF8VYnNFFiroXymJ0ycEBMuYxcZjQQUUHOWruyp65dg?e=PeE8sN),
- rejoindre le slack des coding weeks depuis cette [invitation](https://join.slack.com/t/codingweeks20212022/shared_invite/zt-xvxh6pia-FCIuGk_0jR9Whv9NBqJfAg)
- et rejoindre à minima les canaux `#cw_week1_progweb` et `#cw_important_informations`
 sur Slack.

> Slack est une plateforme de communication collaborative très utilisée en entreprise. C'est par ce moyen que vous pourrez discuter entre vous, partager du code et recevoir des informations complémentaires de la part des encadrants. Vous pouvez soit télécharger l'application Slack ou utiliser la version en ligne.


### Visual Studio Code (VSCode)

Pour ces deux semaines, nous vous recommandons fortement d'installer et d'utiliser [Visual Studio Code](https://code.visualstudio.com/) (à ne pas confondre avec Visual Studio) qui est un éditeur qui s'est beaucoup popularisé ces dernières années. Il est très adapté à python et, surtout, il est très facile à prendre en main et à comprendre. 

Vous pouvez utiliser un autre éditeur si vous le souhaitez. Ce sera alors de votre responsabilité de savoir l'utiliser.

* :point_right: _[Je ne sais pas utiliser VSCode](https://github.com/hudelotc/CentraleSupelec_CodingWeeks_2020/blob/main/VisualStudioCode.md)._
* :point_right: _[Je ne sais pas utiliser VSCode : les raccourcis clavier ](https://github.com/LoicPoullain/je-code/blob/master/utiliser-visual-studio-code.md)._

### Un rapide rappel de Bash

Lors de ces deux semaines, vous allez devoir très souvent utiliser le shell. Nous vous invitons à suivre le petit tutorial ci-dessous pour gagner de l'assurance.


:point_right: _[Cheatsheet Bash](https://github.com/hudelotc/CentraleSupelec_CodingWeeks_2020/blob/main/bash.md)._


### Git

Git est un des outils les plus importants des coding weeks. C'est notamment celui qui vous permettra de travailler à plusieurs sur un même projet informatique.

Pour vous permettre de bien maitriser cet outil, nous vous proposons donc :

* Un cours sur Git qui est disponible [ici](https://web.microsoftstream.com/video/ec2b9aa4-f1c4-42dc-994d-f99b767992d1) ou sur Edunao
* Un petit tutorial à faire sur Git à l'aide de [Learn Git Branching](https://learngitbranching.js.org/) est qui est disponible [ici](https://github.com/hudelotc/CentraleSupelec_CodingWeeks_2020/blob/main/Git.md)


### Python

Suite au cours SIP, vous devriez tous avoir python installé sur votre machine. Si ce n'est pas le cas, nous vous invitons à vous référer aux consignes qui vous ont été données lors de ce cours.

Pour commencer au mieux cette semaine, nous vous proposons de suivre les differents petits tutoriaux ci-dessous sur python :

* :point_right: _[Connaitre et vérifier sa version de python ](https://github.com/hudelotc/CentraleSupelec_CodingWeeks_2020/blob/main/pythonversion.md)._
* :point_right: _[Import de fichiers et de modules
 ](https://github.com/hudelotc/CentraleSupelec_CodingWeeks_2020/blob/main/modulespackagespython.md)._
*  :point_right: _[Exceptions](https://github.com/hudelotc/CentraleSupelec_CodingWeeks_2020/blob/main/exceptions.md)._
 
 
 Avant de passer à la suite, il vous faut passer les 3 tests sur Edunao si ce n'est pas fait :
 
*  [Test bash](https://centralesupelec.edunao.com/mod/quiz/view.php?id=73157)
*  [Test Git](https://centralesupelec.edunao.com/mod/quiz/view.php?id=72936)
*  [Test Jalon 0](https://centralesupelec.edunao.com/mod/quiz/view.php?id=72937)
 








## Semaine 1

Durant cette semaine, des micro-cours seront donnés chaque matin de 9h à 9h30. Le reste du travail se fera en autonomie via les tutoriels ci-dessous (à faire dans l'ordre).

> _Vous pouvez bien évidemment susciter l'aide de l'encadrant si vous êtes bloqué mais n'hésitez pas, dans un premier un temps, à lire les messages d'erreur s'il y en a et à essayer de les résoudre._

### Création d'un dépôt Gitlab

[Suivre le tutoriel Gitlab](./semaine-1/git-and-gitlab.md).

### Configurer l'environnement de développement 

[Suivre le tutoriel sur la configuration de votre environnement de développement](./semaine-1/virtual-environment.md).

### Dévelopment d'une application Web en Django

[Suivre le tutoriel Django](./semaine-1/python-django.md).

<!--
## Semaine 2

**Consignes pour la soutenance**

**Dépôt Gitlab**
- @Loïc Poullain et @celine.hudelot doivent être ajoutés au dépôt en reporter .
- Seule la branche master sera corrigée. Assurez-vous de mettre votre dernière version stable dessus.
- Votre README doit contenir au début la liste des membres et la description du projet.
- Créez un fichier requirements.txt avec la commande pip freeze > requirements.txt pour lister vos dépendances.
- Deadline : cette nuit. Vendredi à 6h, je dois avoir votre dernière version du code sur master.

**Présentation**
- Produisez un seul document Powerpoint pour la présentation. Commitez-le sur votre dépôt et n'oubliez d'en exporter une version PDF. Il doit être commité sur votre dépôt avant la soutenance.
- 15 minutes de présentation (avec une démonstration en direct du produit)
- 5 minutes de questions
- 5 minutes de débrief
- IMPORTANT : soyez ponctuels. Connectez-vous sur le MSTeams de groupe Applications Web 2 à 3 minutes avant votre heure de passage. Votre présentation et votre démo doivent être prêtes. Vous les avez sur un ordinateur de rechange au cas où.

**Notation (à titre indicatif)**
- 1/3 de la note sur la présentation (merci de mettre vos caméras lors de la soutenance), le produit en lui-même et votre gestion de projet et travail en équipe.
- 2/3 de la note sur l'aspect technique
-->
