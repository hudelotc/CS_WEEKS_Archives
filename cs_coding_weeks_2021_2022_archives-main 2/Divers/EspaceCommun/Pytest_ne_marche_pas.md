## Pytest ne marche pas
(FAQ 3A INFONUM)

* As-tu bien Python dans ton PATH ? (voir [problèmes de path](https://github.com/LoicPoullain/je-code/blob/master/regler-les-problemes-de-path.md))
*  As-tu bien la même distribution (version) de Python sélectionnée lors de l'installation de
* As-tu une commande de la forme :
pytest --cov=src --cov-report html tests/test_grid_2048.py
```
* Je veux lancer plusieurs tests :
```
```

Si tu es sous autre chose que Windows, utilise une "wildcard" (*) pour exécuter la commande sur tous les

	* dans le mauvais dossier : tes fichiers tests sont-ils dans un dossier test ? Es-tu
	* dans un shell Windows qui ne supporte pas les wildcards. Utilise
```

Et pour un tuto plus détaillé c'est [ici](https://openclassrooms.com/fr/courses/4425126-testez-votre-projet-avec-python/4435144-ajoutez-des-tests-avec-pytest).