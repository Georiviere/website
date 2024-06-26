# GeoRivière-website
Please gives us a visit at [https://georiviere.fr/](http://georiviere.fr/)


## Publication

Pour toute nouvelle publication, il est important de [respécter une certaine nomenclature](#nommage-des-fichiers).

Les articles se trouvent dans le dossier `_post`:  
https://github.com/Georiviere/website/tree/main/_posts

### Ajout / Modification dans l'interface github

#### Modification
 ![](assets/img/tuto/step-1.png)


#### Ajout d'un nouvel article
 ![](assets/img/tuto/step-2.png)


#### Enregistrement (commit)
Pour sauvegarder les modifications, le nouvel article ou la suppression d'un article, il faut ensuite faire un **Commit**. Il suffit d'indiquer un titre et une description pour (ou laisser le texte par défaut) et cliquer sur "Commit changes".

 ![](assets/img/tuto/step-3.png)


### Nommage des fichiers

Le nom du fichier est très important. Il doit impérativement respecter la syntaxe suivante : `ANNEE-MOIS-JOUR-titre.markdown`. On peut aussi ajouter `-en` ou `-fr` à la fin du titre pour mieux identifier les fichiers en fonction de la langue mais cela n'aura pas d'impact sur le fonctionnement. La date indiquée dans le titre doit être la même que celle du Front Matter.


### Syntaxe / règles à respecter

Chaque article est précédé d'une entête appelé [Front matter](https://jekyllrb.com/docs/frontmatter/). Il est important de respecter certaines règles, comme l'exemple ci-dessous. Le Front Matter se distingue du contenu de l'article avec les `---` qui l'entoure.

```
---
title: Nouveau déploiement de GeoRivière
date: 2022-02-01
lang: en
ref: post-20120201
---
```

- **title** : Le titre de l'article
- **date** : La date de l'article, qui sera affichée sur le site sous la forme "Août 2016". Il est important de respecter le format `aaaa-mm-jj`. Les articles seront ensuite affichés du plus récent en plus ancien.
- **lang** : La langue de l'article
- **ref** : La référence de l'article : sert à identifier les versions traduites des articles. On peut mettre ce qu'on veut, pourvu qu'il soit unique à chaque nouvel article et que sa version en/fr soit identique.

Tout ces paramètres sont obligatoires.


## Développement

### Lancer en local

Nécéssite un environnement Ruby (cf [la doc de Jekyll](https://jekyllrb.com/docs/installation/))

```
bundle install
bundle exec jekyll serve
```
#### Avec docker

```
docker pull jekyll/jekyll:4.2.2
docker run -ti --rm -v .:/srv/jekyll jekyll/jekyll:4.2.2 jekyll build
docker run -ti --rm --volume .:/srv/jekyll -p 4000:4000 jekyll/jekyll:4.2.2 jekyll serve
```
### Publier sur gh-pages

```
git push origin gh-pages
```
<a href="https://territoires.makina-corpus.com/"><img src="https://geotrek.fr/assets/img/logo_makina.svg" alt="Logo MCT" width="125"></a>
