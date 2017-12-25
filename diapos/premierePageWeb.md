# Une première page web en HTML

----

## Les balises HTML et leurs attributs

### Les balises

On ne peut pas simplement écrire du texte dans un éditeur, il faut aussi donner des instructions à l’ordinateur. En HTML, on utilise des balises. Elles sont entourées de chevrons `<` et `>`, comme ceci : `<balise>`. Elles indiquent la nature du texte qu’elles encadrent : ceci est un titre, une image, un paragraphe…

Il y a 2 types de balises :
- les balises en paires : elles s’ouvrent contiennent du texte et se ferment plus loin.
```html
	<titre>Ceci est un titre</titre>
```
- les balises orphelines : ce sont des balises qui servent souvent à insérer un élément à un endroit précis
```html
<image /> ou <image>
```

### Les attributs
Les attributs sont un peu les options des balises, ils les complètent pour donner une information supplémentaire.
```html
<balise attribut="valeur">
  ```
Par exemple avec la balise image, on peut préciser le nom de l’image à afficher :
```html
<image nom="photo.jpg" />
```

Dans les balises fonctionnant par paire, on ne met les attributs que dans la balise ouvrante.

----

## Structure de base d’une page HTML5

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- En-tête de la page -->
        <meta charset="utf-8" />
        <title>Titre</title>
    </head>

    <body>
        <!-- Corps de la page -->
    </body>
</html>
```

`!DOCTYPE`  dit qu’il s’agit d’une page web HTML5.
`html` englobe tout le contenu de la page.  
Une page web est constitué de 2 parties :
- l’en-tête (head) : donne des informations sur la page comme le titre, l’encodage. Ces informations ne sont pas affichés sur la page, ce sont des informations à destination de l’ordinateur. Le contenu de la balise title s’affiche dans l’onglet du navigateur.
- le corps (body) : c’est là que se trouve la partie principale de la page. Tout ce que nous écrivons ici sera affiché à l’écran.

Il est possible d’écrire des commentaires avec les balises. Tout le monde peut voir nos commentaires et tout le code HTML.
```html
 <!-- commentaires -->
 ```
 
