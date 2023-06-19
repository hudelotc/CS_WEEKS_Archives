### Objectif 5 : On améliore notre site.

A ce stade, nous avons un site minimal avec toutes ses briques fonctionnelles. Vous allez maintenant améliorer votre site de différentes manières. Il faudra vous documenter et chercher l'information pour 

  + En travaillant sur le design et les gabarits : Il vous faudra pour cela vous documenter, par exemple [ici](https://docs.djangoproject.com/fr/2.1/ref/templates/language/) et [ici](https://docs.djangoproject.com/fr/1.11/ref/templates/builtins/). Vous pouvez par exemple déjà associer un gabarit ou une partie de vos gabarits à chacune des vues que vous avez créé précedemment.
 Pour cela, il est souvent nécessaire de faire des maquettes du site en avance et en accord avec votre client.
 Vous avez pour cela un certain nombre d'outils comme par exemple :
  + [Canva](https://www.canva.com/fr_fr/creer/maquette-wireframe-site-web/)
  + [MockFlow](https://www.mockflow.com/)
  + [InVision](https://www.invisionapp.com/)
 
 
  + En passant des paramètres et donc vos données à vos gabarits via les vues, le fichier `views.py` et la méthode `render`qui prend en premier paramètre un dictionnaire de variables à utiliser dans le gabarit. 
  
 Par exemple, pour la page d'accueil et la vue lui correspondant, on peut mettre à jour la méthode `index`de la manière suivante :

```python
def index(request):
    products = Product.objects.filter(available=True).order_by('-created_at')[:12]
    ...
    context = {
        'products': products
    }
    return HttpResponse(template.render(context, request=request))
```

et en l'affichant dans le gabarit (dans le fichier `.html`) via la syntaxe :

```html
<ul>
{% for product in products %}
    <li>{{ products }}</li>
{% endfor %}
</ul>
```

 + En générant automatiquement les url dans votre fichier de gabarit. Par exemple, supposons que vous ayez généré l'URL pattern suivant dans votre fichier `urls.py`, pour permettrr d'avoir une page pour produit (on veut par exemple afficher le détail de chaque produit). Vous auriez dans votre fichier `urls.py`:

```python
 ...
urlpatterns = [
    url(r'^(?P<product_id>[0-9]+)/$', views.detail, name='detail'),
]
```
Il vous faut maintenant ajouter dans le fichier html correspondant le code suivant :

```html
<a href="{% url 'detail' product_id=product.id %}">
  <img class="img-responsive" src="{{ product.image }}" alt="{{ product.title }}">
</a>
```
Cela suppose bien entendu que vous avez ajouté un champ `image` à votre modèle de produits.


 + En ajoutant un [formulaire de recherche](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1607171-les-formulaires) à votre site web. 

 Il faudra pour cela que vous ajoutiez un gabarit `search_form.html`, dans lequel vous écrirez un formulaire de recherche.
 
 ```html
 <div class="col-lg-12 detail-separator">
  <form class="col-md-6 col-md-offset-3 text-center" action="{% url 'store:search' %}" method="get" accept-charset="utf-8">
    <div class="form-group">
      <label for="searchForm">Chercher un produit</label>
      <input id="searchForm" class="form-control">
    </div>
    <span class="help-block" id="helpBlock">Donner son nom et son producteur.</span>
  </form>
</div>
 ```
 
 que vous pourrez par exemple inclure dans votre fichier `index.html` via la commande :
 
 `{% include 'store/search_form.html' %} <!-- NEW -->`
 
La [documentation](https://docs.djangoproject.com/en/2.1/) de Django est très bien faite donc n'hésitez pas à la parcourir.

Faites un maximum, pensez à bien tester votre code et à déposer sur votre dépôt le code de votre site.




  
 




