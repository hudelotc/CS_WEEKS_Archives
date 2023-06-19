# SaclayLocal - Sprint 0 : Reflexion autour de la conception

Après cette phase d'analyse, nous pouvons avoir une première démarche de conception et essayer d'identifier les principaux objets de notre MVP. 

La question à se poser c'est *De quoi parle t'on ?* 

## Vers un langage commun

Dans cette phase de reflexion sur la conception, pour favoriser le travail collaboratif et une compréhension commune entre tous les membres du projets, il est important de définir, dès le début du projet, un **vocabulaire commun** autour des termes métier. Dans le jargon du developpement de logiciel, on parle de [**ubiquitous language**](http://referentiel.institut-agile.fr/ubiquitous.html) ou **langage omniprésent**. C'est un principe issu de l'approche *Domain Driven Design* décrite dans l'[ouvrage](https://github.com/p0w34007/ebooks/blob/master/Eric%20Evans%202003%20-%20Domain-Driven%20Design%20-%20Tackling%20Complexity%20in%20the%20Heart%20of%20Software.pdf) du même nom et qui consiste à identifier et à définir un langage commun autour des termes métiers ce qui peut être [utile](https://promyze.com/pourquoi-lire-red-book-domain-driven-design/) dans de nombreuses situations.


Dans le cas du projet *saclaylocal*, c'est un travail qui vous sera très utile car votre projet implique des développeurs et des experts métiers (les producteurs, la commauté Paris Saclay, les consommateurs). Ce projet est un projet scolaire et il n'y a donc pas d'expert métiers impliqués sur ce projet mais pour essayer de faire comme si, vous pouvez par exemple imaginer que votre client est la chambre de commerce de ParisSaclay qui souhaite mettre en avant la consommation locale.


Le déroulé consiste à produire ce que l'on appelle des [**User Stories**](https://en.wikipedia.org/wiki/User_story) (avec l'ensemble des parties prenantes du projet) qui représentent les besoins des utilisateurs à implémenter. Ce travail permet aussi de définir le langage partagé.

Une **user story** ce n'est rien d'autre qu'une phrase simple, en language naturel, qui permet de décrire le contenu d'une fonctionnalité à développer en précisant le *Qui?*, le *Quoi?* et le *Pourquoi?*

 `En tant que <qui>, je veux <quoi> afin de <pourquoi>`

Ici, typiquement : 

+ En tant que producteur , je veux pouvoir **m'inscrire pour pouvoir mettre mon catalogue de produits en ligne** sur le site
+ En tant que producteur, je veux pouvoir **choisir une quantité de produits** et  **fixer un prix** à **mes produits**.
+ En tant que producteur, je veux pouvoir avoir une **changer le prix d'un produit**.
+ En tant que consommateur, je veux pouvoir **voir une listes de produits disponibles** par **producteur**, **par type** ...
+ En tant que consommateur, je veux pouvoir **constituer un panier** et le **sauvegarder**.
+ ...


Ici, les termes et expressions **catalogue**, **panier**, **produit** par exemple font partie du **langage partagé** de notre contexte. Ils pourront être utilisés indifféremment par l’ensemble des acteurs projets et désigneront toujours les mêmes concepts.

La finalité ici est de simplifier les échanges entre les différents acteurs, quelqu'ils soient.

Ils doivent aussi vous permettre de bien nommer les différents objets, variables, fonctions de votre application.

Nous ne répondrons bien sûr pas à toutes ces user-stories dans le cadre de ce projet de semaine 1 mais en terme de métholologie, ce travail est un travail à faire très tôt dans la construction d'un projet de developpement informatique : **discuter avec les parties prenantes**.

## Les principaux objets, modules de votre application

Cette phase d'analyse doit aussi vous faire reflechir à la conception de votre application et notamment aux différents objets et modules de cette dernière en essayant de séparer les responsabilités. 

Pour cela, essayez de réflechir à l'architecture fonctionnelle de votre application et à comment les différents acteurs, modules, objets intéragissent entre eux. Faites le avec un papier et un crayon, de manière schématique. Un travail et une reflexion de groupe peut être intéressante ici !

Prenez un peu de temps pour faire ce travail. Une fois terminé, prenez une photo de ce que vous avez mis sur papier et stockez cela dans un répertoire intitulé `WorkingDocs`de votre dépôt git. N'oubliez pas de faire un `commit` et de mettre à jour votre dépôt distant.

 
L'objectif de ce travail est de vous permettre de modéliser, du point de vue informatique, votre problème mais il est essentiel aussi pour l'organisation de votre travail, c'est-à-dire, son découpage en différents sprints et fonctionnalités par exemple. 

Ici, ce travail a été fait pour vous mais, il faudra le faire pour votre projet de la semaine 2.


<span style="color: #26B260">**A ce stade du projet, vous avez atteint le JALON 2 : Analyse et Conception de mon produit**</span>.



Nous allons maintenant passer à l'étape de développement par la réalisation de la [**Fonctionnalité 1** : Prise en main de Django : création d'un projet Django.](./S1_djangoproject.md)
