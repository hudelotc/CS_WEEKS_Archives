# Semaine 1 - Configurer l'environnement de développement 

Nous allons à présent vérifier la configuration de votre environnement.

## Vérification des installations

Vérifions d'abord que tout est bien installé.

Si vous ne l'avez pas déjà fait, installez [python 3](https://www.python.org/downloads/).

Ouvrez ensuite un terminal et exécutez la commande suivante :

> Si vous êtes sur Windows, votre terminal s'appelera "Invite de commandes", "cmd", "Git bash" ou "Powershell". Par simplicité, le terme "terminal" sera utilisé par la suite.

```bash
python --version
pip --version
```

Vous devriez obtenir un résultat de cette forme.

```bash
Python 3.7.6
pip 20.2.3
```

Si ce n'est pas le cas, merci de suivre un des liens ci-dessous :

:point_right: [J'obtiens une erreur quand j'exécute ces commandes](https://github.com/LoicPoullain/je-code/blob/master/regler-les-problemes-de-path.md).

:point_right: [La version affichée de python n'est pas la version 3](https://github.com/LoicPoullain/je-code/blob/master/connaitre-sa-version-de-python.md).

<!--## Création et activation de l'environnement virtuel (optionel)

A présent que nous nous sommes assuré que `python` et `pip` étaient bien installés et accessibles, nous allons configurer notre environnement virtuel.

Pour cela, nous utiliserons la librairie `virtualenv`:

```bash
pip install virtualenv
```

Maintenant créez votre environnement virtuel (nous supposons ici que vous êtes à la racine de votre dépôt Git) :

```bash
virtualenv venv
```

Votre environnement est maintenant créé. Vous pouvez l'activer avec la commande suivante. Cette commande devra être exécutée à chaque fois que vous ouvrirez un nouveau terminal.

*Mac OS, Linux*
```bash
source venv/bin/activate
```

*Windows*
```bash
venv\Scripts\activate
```

> Pour quitter votre environnement virtuel, il vous suffira d'exécuter la commande suivante :
>
> ```bash
> deactivate
> ```
-->

## Ajout d'une dépendance

Maintenant que notre environnement de développement est configuré, nous sommes prêts à installer Django:

```bash
pip install django
```

:point_right: [Je n'arrive pas à installer Django](https://github.com/LoicPoullain/je-code/blob/master/probleme-installation-django.md).
