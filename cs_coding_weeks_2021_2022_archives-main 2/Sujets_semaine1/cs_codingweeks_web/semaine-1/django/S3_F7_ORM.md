# Fonctionnalité 7 : Création de notre modèle avec l'ORM Django



## Etape 1 : création de tables

Pour créer votre modèle dans Django, en accord avec le modèle MVT, vous allez ouvir le fichier `models.py`.

Comme nous sommes dans une problématique de modélisation, Django fait appel aux paradigmes de la [programmation orientée objet(POO)](https://openclassrooms.com/fr/courses/4302126-decouvrez-la-programmation-orientee-objet-avec-python) de python et ainsi dans Django, chaque table est représentée par une classe. Il ne vous est pas demandé de vous former à la POO ici et des exemples vous sont donc donnés pour vous aider à créer votre modèle.


Prenons par exemple la table `Producer` et considérons qu'elle a un champ `ID` et un champ `name` . Pour la représenter en Django, nous allons créer une nouvelle classe `Producer` en suivant la syntaxe ci-dessous :

```python
from django.db import models

class Producer(models.Model):
    name = models.CharField(max_length=200, unique=True)
```
La deuxième ligne `name=models.CharField(max_length=200, unique=True)` indique qu'elle a un attribut de type chaîne de caractères de longueur maximum 200 et que sa valeur est unique. Django génère automatiquement le champ ID et il n'est donc pas utile de le déclarer.

Cette classe representera la table correspondante dans la base de données.
Créer maintenant le modèle Django correspondant au modèle que vous avez conçu à l'étape précédente. On s'occupera des relations dans l'étape suivante.
 Nous vous conseillons de vous référer à la documentation de Django [ici](https://docs.djangoproject.com/fr/1.11/topics/db/models/). Il y a de nombreux [types prédéfinis](https://docs.djangoproject.com/fr/1.11/ref/models/fields/) comme par exemple le champ `EmailField`  utile pour representer des adresses mails (quel site ne demande pas l'adresse mail aujourd'hui ?).

## Etape 2 : Ajout des relations



Django fournit aussi la possibilité de représenter des relations :

 + **relation un à un (one to one)**.  Cette relation se déclare avec la classe [`OnetoOneField`](https://docs.djangoproject.com/fr/2.1/topics/db/examples/one_to_one/) dans la classe qui contient la clé étrangère. Par exemple supposons une relation un à un entre un `Produit` et une réservation de ce produit (on met le produit dans le panier) que l'on représentera par la classe `Basket` alors la classe `Basket` possédera la déclaration suivante dans sa définition:

```python
 class Basket(models.Model):
    ...
    product = models.OneToOneField(Product)
 ```
 
 + **relation plusieurs à un (many to one)**. Cette relation se déclare avec la classe [`ForeignKey`](https://docs.djangoproject.com/fr/2.1/topics/db/examples/many_to_one/). Supposons par exemple que nous avons une classe `Client` correspondant à une table `Client` et que nous voulons modéliser la relation entre un client et un panier. C'est une relation **plusieurs à un**, un client peut avoir plusieurs mais un panier ne peut être qu'à un seul client.

```python
 class Basket(models.Model):
    ...
    client = models.ForeignKey(Client, on_delete=models.CASCADE)
    product = models.OneToOneField(Product)
```   
 
 + **relation plusieurs à plusieurs (many to many)**. Cette relation se déclare avec la classe [ManyToManyField](https://docs.djangoproject.com/fr/2.1/topics/db/examples/many_to_many/). Supposons par exemple que le site permet de representer une relation entre les Clients et les Producteurs. On aurait la syntaxe ci-dessous :

```python
 class Producer(models.Model):
    name = models.CharField(max_length=200, unique=True)
    clients = models.ManyToManyField(Client, related_name='producers', blank=True)

 ```

Vous devez maintenant finir de créer le modèle Django correspondant au modèle que vous avez conçu à l'étape précédente.

N'oubliez pas de : 

+ <span style='color:blue'>Faire un commit de vos changements sur votre dépôt local.</span> 
+ <span style='color:blue'>Pousser (Push) votre code vers votre dépôt distant sur GitLab.</span> 


Et nous allons maintenant compléter notre application en passant à la [**Fonctionnalité 8** : Mise en place des migrations entre Django et la base de données](./S4_F8_migrations.md)




