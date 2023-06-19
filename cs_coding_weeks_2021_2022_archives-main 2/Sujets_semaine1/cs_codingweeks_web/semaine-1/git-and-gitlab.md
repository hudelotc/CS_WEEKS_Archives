# Semaine 1 - Création d'un dépôt Gitlab

Pour partager votre code entre vous et avec l'encadrant, vous allez utiliser *Git* et *Gitlab* durant ces deux semaines.

> _Git_ est une solution opensource pour gérer les différentes versions d'un code et se les partager.

> _Gitlab_ et _Github_ sont des plateformes web collaboratives qui s'appuient sur Git. C'est par Gitlab qui vous stockerez votre code à distance et que votre binôme et le correcteur y auront accès.

### Vérification des installations

Avant de commencer, nous allons vérifier que Git est bien installé et configuré sur votre ordinateur.

Si vous ne l'avez pas déjà fait, installez [Git](https://git-scm.com/).

Ouvrez ensuite un terminal et exécutez la commande suivante :

> Si vous êtes sur Windows, votre terminal s'appelera "Invite de commandes", "cmd", "Git bash" ou "Powershell". Par simplicité, le terme "terminal" sera utilisé par la suite.

```bash
git --version
```

Vous devriez obtenir un résultat de cette forme.

```bash
git version <numéro de version>
```

:point_right: _[J'obtiens une erreur quand j'exécute ces commandes](https://github.com/LoicPoullain/je-code/blob/master/regler-les-problemes-de-path.md)_.

### Introduction à Git et Gitlab

Une fois cette vérification effectuée, suivez les deux tutoriels ci-dessous pour apprendre à utiliser Git et Gitlab. L'un est une vidéo et l'autre est sur Github :

- https://web.microsoftstream.com/video/ec2b9aa4-f1c4-42dc-994d-f99b767992d1
- https://github.com/hudelotc/CentraleSupelec_CodingWeeks_2020/blob/main/Git_install.md

### Création d’un dépôt Gitlab commun

Si vous avez suivi correctement le tutoriel précédent, vous devriez maintenant avoir un dépôt sur Gitlab partagé avec votre binôme. N'oubliez pas d'ajouter les encadrants (i.e @loic.poullain et @celine.hudelot) comme `reporter` à votre dépôt.

:point_right: _[Je n'ai pas réussi à créer mon dépôt commun](https://github.com/LoicPoullain/je-code/blob/master/configurer-depot-gitlab.md)_.

<!-- ### Apprendre à gérer les conflits

TODO: provoquer et gérer des conflits -->


### Test de connaissance

Une fois fait, rendez-vous sur EDUNAO pour passer ce [test](https://centralesupelec.edunao.com/mod/quiz/view.php?id=72936) de compréhension (obligatoire).

### Ajout d'un `.gitignore`

Notre dépôt Gitlab est presque prêt. Il nous reste maitenant à ajouter un `.gitignore`.

Il y a certain nombre de fichiers que nous ne voudrons pas *commiter* durant ce TP. Il s'agit de la base de données, des fichiers *cache* de python se terminant par `*.pyc` ou encore de ceux gérant notre futur environnement virtuel.

Pour les ignorer à l'avenir (et ne pas avoir de douloureux conflits à gérer), ajoutez un fichier `.gitignore` à votre dépôt avec le contenu suivant :

```
.DS_Store
__pycache__
*.pyc
db.sqlite3
venv
```

:point_right: _[J'ai ignoré cette étape et j'ai maintenant des problèmes avec Git](https://github.com/LoicPoullain/je-code/blob/master/ajout-gitignore.md)_.

<span style="color: #26B260">**A ce stade du projet, vous avez atteint le JALON 1.**</span>