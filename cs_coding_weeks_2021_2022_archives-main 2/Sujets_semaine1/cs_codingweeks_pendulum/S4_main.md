# Fonctionnalité 6 : On met tout cela dans un programme principal


A ce stade, nous avons bientôt fini notre MVP, c'est à dire un programme qui peut charger des images de personnes, détecter les visages (bouding box) et reconnaître à qui appartient le visage.

Imaginez que vous devez préparer une démonstration pour votre client. Il va alloir peu *packager* votre code pour le rendre un peu plus professionnel. 

Une des premières étapes est d'associer à votre projet un programme principal. Vous pouvez par exemple, ajouter à la racine de votre projet un fichier `dataviz_main.py` qui contiendra le point d'entrée des scripts.

Autrement dit, nous voulons pouvoir lancer la démonstration de notre MVP, en exécutant le fichier `facerecognition_main.py`.

En ligne de commande, cela donnerait :

`python facerecognition_main.py``



Pour cela il faut donc ajouter une fonction principale dans  `dataviz_main.py` de la manière suivante : 

```PYTHON
if __name__ == '__main__':
...

```
Et à l'intérieur du bloc, il faudra donc :

 + Charger les données
 + Les prétraiter
 + Détecter les visages
 + Les reconnaître



Un peu de documentation [ici](http://interactivepython.org/runestone/static/CS152f17/Functions/mainfunction.html) et [là](https://www.guru99.com/learn-python-main-function-with-examples-understand-main.html) pour vous aider dans l'écriture de ce programme.

A ce stade, vous pouvez aussi vous poser la question de la ré-utilisation de votre code.
Typiquement, pour ce projet, l'équipe encadrante devrait pouvoir cloner votre projet du dépôt distant et exécuter vos programmmes sans bugs.


+ Il faut, pour éviter tout problème, que votre code soit bien structuré ou architecturé et bien écrit (par exemple, en privilégiant des chemins d'accès relatifs aux fichiers aux chemins absolus).
+ Il faut aussi dire quels sont les dépéndances de votre projet, typiquement, toutes les bibliothèques externes qui sont nécessaires. La manière typique de faire est de créer un fichier `requirements.txt` listant tous les packages nécessaires avec leur version.

```
matplotlib =='3.1.1'
...
```
Il est donc nécessaire de lister toutes les dépendances et leur version dans ce fichier. Il suffira alors à un utilisateur de lancer la commande ci-dessous pour installer les dépendances.

`pip install -r requirements.txt`


Sur cet aspect, si vous voulez aller plus loin, vous pouvez aussi regarder ce [tutoriel](https://techblog.deepki.com/package-management-tools/). 


+ Enfin, il sera nécessaire de documenter un peu votre `README.md` pour justement écrire les consignes d'éxecution.

Prenez le temps de faire ce travail, documenter votre code et bien sûr :

+ <span style='color:blue'>Faire un commit de vos derniers changements.</span> 
+ <span style='color:blue'>Tagger ce dernier commit </span> 
+ <span style='color:blue'>Pousser (Push) votre code vers votre dépôt distant sur GitLab.</span> 

Un bon test ici est de demander à une personne de votre groupe de cloner votre code sur votre dépôt distant et d'executer votre projet en suivant les consignes données dans votre README.

Pour finaliser ce MVP, une dernière étape est de founir à notre MVP une interface en ligne de commande. C'est l'objet de la [**Fonctionnalité 7** : Une interface en ligne de commande avec `argparse`.](./S3_argparse.md)






