# Fonctionnalité 12: Integrer les fichiers statiques à l'application.



## Etape 1 : intégrer le thème dans votre projet

Pour intégrer les fichiers statiques du thème choisi à votre application, c'est assez simple. Il suffit de :

 + Créer une dossier `static` à l'intérieur de votre application `store` et d'y ajouter un nouveau dossier du nom de l'application.  
 + Déplacer les feuilles de styles (css), le javascript (js), les polices de caractères et les images du thème choisi. 

 
## Etape 2 : Rendre un gabarit dans une vue
 
Pour cette étape, il faut :

 +  Ouvrez le dossier html du thème ou le fichier html du thème.
 +  Copiez l'intégralité du HTML contenu dans index.html et collez le dans un fichier `index.html` que vous mettrez dans le dossier `templates/store` de votre application `store`.

 
 Il vous faut maintenant modifier le fichier `views.py` en mettant à jour la fonction `index` de telle sorte qu'elle affiche ce fichier `index.html`
 
 ```python
 from django.template import loader
 def index(request):

    template = loader.get_template("./store/index.html")
    return HttpResponse(template.render(request=request))
 
  ```
  
## Etape 3 : mettre à jour les styles.

La dernière chose à faire est de mettre à jour les styles dans le fichier index.html que vous venez de créer.

Il faut en particulier remplacer :

```html
<!-- Bootstrap Core CSS -->
<link href="css/bootstrap.min.css" rel="stylesheet">

<!-- Custom CSS -->
<link href="css/business-casual.css" rel="stylesheet">

...


<!-- jQuery -->
<script src="js/jquery.js"></script>

<!-- Bootstrap Core JavaScript -->
<script src="js/bootstrap.min.js"></script>
```

Par 

```html
{% load static %}

<!-- Bootstrap Core CSS -->
<link rel="stylesheet" type="text/css" href="{% static 'store/css/bootstrap.min.css' %}" />
<!-- Custom CSS -->
<link rel="stylesheet" type="text/css" href="{% static 'store/css/business-casual.css' %}" />

...

<!-- jQuery -->
<script src="{% static 'store/js/jquery.js' %}"></script>

<!-- Bootstrap Core JavaScript -->
<script src="{% static 'store/js/bootstrap.min.js' %}"></script>
 ```
 
 
 
 