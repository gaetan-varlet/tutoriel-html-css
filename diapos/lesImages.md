# Les images

----

## Les différents formats d’images
utiliser le JPEG pour les photos  
utiliser le PNG pour les graphiques  
utiliser le GIF animé pour les images animées  

Bannir les autres formats comme le BMP.  
Bien choisir le nom des images : en minuscules, sans espace ni accent. Par exemple : mon_image.png.

----

## Insérer une image

###Insertion d’une image
Il faut utiliser la balise `<img />`. C’est une balise orpheline. 2 attributs sont obligatoires :
- `src` : pour indiquer où se trouve l’image. Il faut indiquer soit le chemin absolu, soit le chemin relatif
`alt` : texte alternatif. On doit toujours indiquer un texte alternatif qui est un court texte qui décrit ce que contient l’image. Ce texte sera affiché à la place de l’image si celle-ci ne peut pas être téléchargé ou dans les navigateurs de personnes handicapées. Pour une image de fleur, on mettrait par exemple `alt=”Une fleur”`.

Les images doivent se trouver obligatoirement à l’intérieur d’un paragraphe.
```html
<p>
    Voici une photo que j'ai prise lors de mes dernières vacances à la montagne :<br />
    <img src="images/montagne.jpg" alt="Photo de montagne" />
</p>
```

### Ajouter une infobulle
L’attribut permettant d’afficher une bulle d’aide est le même que pour les liens : `title`. C’est un attribut facultatif. Survolez la photo avec la souris pour voir l’infobulle apparaître.
```html
<p>
    Voici une photo que j'ai prise lors de mes dernières vacances à la montagne :<br />
    <img src="images/montagne.jpg" alt="Photo de montagne" title="C'est beau les Alpes quand même !" />
</p>
```

### Miniature cliquable
Si votre image est très grosse, il est conseillé d’en afficher la miniature sur notre site. Ajoutez ensuite un lien sur cette miniature pour que vos visiteurs puissent afficher l’image en taille originale.
Placer les 2 images dans un dossier img par exemple : montagne.jpg et montagne_mini.jpg.
```html
<p>
    Vous souhaitez voir l'image dans sa taille d'origine ? Cliquez dessus !<br />
    <a href="img/montagne.jpg"><img src="img/montagne_mini.jpg" alt="Photo de montagne" title="Cliquez pour agrandir" /></a>
</p>
```

----

## Les figures
Ce sont des éléments qui viennent enrichir le texte pour compléter les informations de la page.

Les figures peuvent être de différents types :
- images
- code source
- citations
- etc…

Bref, tout ce qui vient illustrer le texte est une figure.

### Création d’une figure
En HTML5, on dispose de la balise `<figure>`.
```html
<figure>
    <img src="images/blocnotes.png" alt="Bloc-Notes" />
</figure>
```

Une figure est le plus souvent accompagné d’une légende. Il faut utiliser la balise `<figcaption>` à l’intérieur de la balise `<figure>`.
```html
<figure>
    <img src="images/blocnotes.png" alt="Bloc-Notes" />
    <figcaption>Le logiciel Bloc-Notes</figcaption>
</figure>
```

### Bien comprendre le rôle des figures
Il faut plutôt placer une image dans un paragraphe si elle n’apporte aucune information, que c’est juste une illustration pour décorer.
Il faut la placer dans une figure si elle apporte de l’information.
En effet la balise `<figure>` a un rôle avant tout sémantique, cela veut dire qu’elle indique à l’ordinateur que l’image a du sens et qu’elle est importante pour la bonne compréhension du texte.
