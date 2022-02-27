# La couleur et le fond

## Couleur de texte

La propriété CSS s’appelle **color**.

Les valeurs peuvent être indiquées de différentes façons :
- indiquer le nom des couleurs : *white, black, red…* (16 couleurs en CSS)
- en hexadécimale (`#` suivi de 6 lettres ou chiffres), par exemple `#FF5A28`
- la méthode RGB (Rouge-Vert-Bleu) avec des valeurs comprises entre 0 et 255 : `rgb(240,96,204)`

----

## Couleur de fond

- On utilise la propriété CSS **background-color**. Elle s’utilise de la même manière que la propriété color.
- Pour indiquer la couleur de fond de la page web, il faut travailler sur la balise `<body>`.
- On peut modifier la couleur de fond de la page mais aussi d’autres éléments : des titres, des paragraphes, des mots… Dans le cas des mots, ils apparaîtront surlignés.

----

## L’héritage en CSS

- En CSS, si vous appliquez un style à une balise, toutes les balises se trouvant à l’intérieur prendront le même style.
- Si on modifie le style de la balise `<body>`, le style des balises `<p>` et `<h1>` sera aussi modifié.
- On dit que les balises qui se trouvent à l’intérieur d’une autre balise héritent de ses propriétés.
- C’est l’élément le plus précis qui a la priorité. Par exemple, la couleur de fond de la balise `<mark>` sera prioritaire sur la couleur de fond de la balise `<body>`.
- Le même principe vaut pour toutes les balises HTML et CSS.

----

## Images de fond

- Il est possible de mettre une image de fond sur la page, mais aussi sur un titre, un paragraphe…
- La propriété permettant d’indiquer le fond est **background-image**. Comme valeur, on doit renseigner *url(“nom_de_l_image.png”);*

```css
body
{
    background-image: url("neige.png");
}
```

Des options sont disponibles pour changer le comportement de l’image de fond :
- **background-attachment** : fixer le fond. On voit alors le texte glisser par-dessus le fond.
  - *fixed* où l’image de fond reste fixe
  - *scroll* (par défaut) qui fait défiler l’image de fond avec le texte.
- **background-repeat** : répétition du fond (par défaut l’image est répétée en mosaïque).
  - *no-repeat* : le fond ne sera pas répété, l’image sera donc unique sur la page
  - *repeat-x* : le fond sera répété uniquement sur la première ligne, horizontalement
  - *repeat-y* : le fond sera répété uniquement sur la première colonne, verticalement.
  - *repeat* : le fond sera répété en mosaïque (par défaut)
- **background-position** : position du fond. On peut indiquer où se trouve l’image de fond. Intéressant uniquement si combiné avec `background-repeat: no-repeat;`.
Il faut donner deux valeurs en pixels pour indiquer la position du fond par rapport au coin supérieur gauche.
```css
{background-position: 30px 50px;}
```
Il est aussi possible d’utiliser les valeurs suivantes en anglais, seules ou combinées : *top, bottom, left, center, right*
```css
{background-position: top right;}
```

### Combiner les propriétés

Par exemple, pour afficher un soleil en image de fond, en un unique exemplaire toujours visible et positionné en haut à droite, on peut écrire :

```css
body
{
    background-image: url("soleil.png");
    background-attachment: fixed; /* Le fond restera fixe */
    background-repeat: no-repeat; /* Le fond ne sera pas répété */
    background-position: top right; /* Le fond sera placé en haut à droite */
}
```

S’il y a beaucoup de propriétés comme dans cet exemple, on peut utiliser une “super-propriété” appelée **background** dont la valeur peut combiner plusieurs des propriétés vues précédemment. On peut donc écrire simplement :
```css
body
{
    background: url("soleil.png") fixed no-repeat top right;
}
```

Il y aura d’autres super-propriétés par la suite. Il faut savoir que :
- l’ordre des valeurs n’a pas d’importance. Vous pouvez combiner les valeurs dans n’importe quel ordre.
- vous n’êtes pas obligés de mettre toutes les valeurs.

### Plusieurs images de fond

Depuis CSS3, il est possible de donner plusieurs images de fond à un élément. Pour cela, il suffit de séparer les déclarations par une virgule. La première image sera placée par dessus les autres.
```css
body
{
    background: url("soleil.png") fixed no-repeat top right, url("neige.png") fixed;
}
```

----

## La transparence

Le CSS3 nous permet de jouer facilement avec le niveau de transparence des éléments, avec la propriété **opacity** et la notation RGBa.

### La propriété opacity
La propriété opacity permet d’indiquer le niveau d’opacité (l’inverse de la transparence) :
- avec une valeur de 1, l’élément sera totalement opaque (par défaut)
- avec une valeur de 0, l’élément sera totalement transparent.

Il faut donc choisir une valeur comprise entre 0 et 1. Une valeur de 0.6 fera que notre élément est opaque à 60%.
```css
p
{
    opacity: 0.6;
}
```

### La notation RGBa
Il s’agit de la notation RGB avec un quatrième paramètre : le niveau de transparence. De la même façon que précédemment, avec une valeur de 1, le fond est complètement opaque.
```css
p
{
    background-color: rgba(255, 0, 0, 0.5); /* Fond rouge à moitié transparent */
}
```
