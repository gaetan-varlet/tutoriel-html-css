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
 
----

## L'en-tête <head>

Il s'agit d'informations sur la page web : les métadonnées du document
- `<title>Titre</title>` : titre de la page, utilisé par les moteurs de recherche
- `<meta>` : balise vide qui prend des attributs
    - **charset** pour préciser l'encodage
    - **description** : description de la page dans les moteurs de recherche
- `<link>` : balise vide pour faire le lien avec une ressource externe, par exemple le *CSS*, ou la *favicon*
    - **rel** : type de lien
    - **href** : lien de la ressource
- `<script>` permet d'écrire directement du JS
- `<style>` permet d'écrire directement du CSS


```html
<head>
    <meta charset="utf-8" />
    <meta name="description" content="ma description...">
    <title>Titre</title>
    <link rel="stylesheet" href="style.css" />
    <link rel="favicon" href="style.css" />
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
```

----

## L'encodage

- l'ordinateur travaille en binaire, groupé en groupe de 8 bits, 1 octet en français (1 byte en anglais)
- 1 octet permet de représenter 2^8 caractères, 256 possibilités, des nombres allant de 0 à 255
- le principe de l'encodage est de faire correspondre un octet à un caractère de notre alphabet
- la table ASCII (American Standard) utilise 7 bits (128 nombres), par exemple `a` correspond au nombre 97. Cette table ne gère pas les caractères accentués
- la table Windows-1252, utilise 8 bits, contient donc d'autres caractères, notamment les caratères accentués européens
- chaque pays avait son propre encodage, pour simplifier la compatibilité est arrivée le **jeu de caractères** **Unicode** qui contient tous les caractères du monde (ce n'est pas un encodage)
- il est basé sur les 128 premiers caractères ASCII
- le symbole `€` n'est pas à la même position en Unicode (position 8364) qu'en Windows-1252 (position 128)
- l'encodage **UTF-8** va représenter les nombres de 0 à 127 sur 1 seul octet, à partir d'une certaine valeur 2 octets, puis 3 octets et 4 octets
- il y a un nombre dynamique d'octets selon le caractère à représenter, pour éviter d'encoder tous les caractères sur plusieurs octets pour ne pas utiliser de l'espace inutilement
- pour savoir si le caractère est représenté par un ou plusieurs octets, on utilise les premiers bits d'un octet
- avec l'UTF-8, il n'est plus possible de compter le nombre d'octets pour connaître le nombre de caractères, le calcul est un peu plus compliqué
- l'UTF-16 se base sur le même principe de tailles variables mais encode les caractères sur 2 octets par défaut
- l'UTF-32 est un encodage où chaque caractère est codé sur 4 octets
