# Fonctionnalité 10 : Mettre à jour les vues pour afficher les données de la base de données


L'objectif ici est de mettre à jour toutes nos vues pour qu'elles affichent des informations issues de la base de données.

Il faut pour cela ouvrir le fichier `views.py` de votre application.

## Etape 1 : Mise à jour de la page d'accueil

Modifier votre fonction `index(request)`de telle sorte que vous affichiez l'ensemble des produits disponibles sur la page d'accueil au moment du lancement de l'application.

Vous pourrez par exemple utiliser la fonction `filter` en suivant l'exemple ci-dessous.

```python
def index(request):
    products = Product.objects.all()
    formatted_products = ["<li>{}</li>".format(product.name) for product in products]
    message = """<ul>{}</ul>""".format("\n".join(formatted_products))
    return HttpResponse(message)

```

Vous pouvez essayer d'ajouter des objets en même temps dans votre base via la console Django puis raffraichir votre page. Qu'observez vous ?

## Etape 2 : Mise à jour de la deuxième vue.

Modifier votre fonction `detail_product` pour afficher les détails d'un produit donné. Regarder par exemple la méthode [`get`](https://docs.djangoproject.com/fr/2.1/topics/db/queries/).


## Etape 3 : Mise à jour la page de recherche

Vous devez ici mettre à jour la fonction `search` pour prendre en compte votre modèle .

## Etape 4 : A vous de jouer ! 

Ajouter ce qu'il vous semble utile à votre site en fonction de votre modèle et des vues que vous souhaiteriez avoir pour votre application.
Quand vous avez fini, comme nous sommes à la fin d'un sprint : 



+ <span style='color:blue'>Faire un commit .</span> 
+ <span style='color:blue'>Tagger à la fin de chaque journée votre dernier commit </span> 
+ <span style='color:blue'>Pousser (Push) votre code vers votre dépôt distant sur GitLab.</span> 
+ <span style='color:blue'>Faire un test de couverture de code.</span>



Nous allons maintenant améliorer le design de notre site WEB en passant à la fonctionnalité [**Fonctionnalité 11** : Choisir un theme pour notre application](./S6_F11_statictheme.md).

