# Le responsive design avec les Media Queries
Les media queries sont des règles à appliquer pour changer le design d’un site en fonction des caractéristiques de l’écran. On peut donc charger des styles CSS différents. Grâce à cette technique, nous pourrons créer un design qui s’adapte automatiquement à l’écran de chaque visiteur !

---

## Mise en place des media queries

C’est une nouveauté de CSS3. Ce n’est pas une propriété mais des règles que l’on peut appliquer dans certaines conditions, comme dire si la résolution de l’écran du visiteur est inférieure à tant, alors applique les propriétés CSS suivantes. Il est alors possible de changer l’apparence du site comme augmenter la taille du texte, changer la couleur de fond, position différemment le menu, etc…
Les conditions sont la résolution mais on peut aussi utiliser le type d’écran (smartphone, télévision, projecteur…), le nombre de couleurs, l’orientation de l’écran (portrait ou paysage), etc…

**Appliquer une media query**
Les media queries sont donc des règles qui indiquent quand on doit appliquer des propriétés CSS. Il y a deux façons de les utiliser :
- en chargeant une feuille de style .css différente en fonction de la règle, par exemple, si la résolution est inférieure à 1280px de large, charge le fichier *petite_resolution.css*. On ajoute une deuxième balise `<link />` pour charger le fichier CSS
```html
<!-- Pour tout le monde -->
<link rel="stylesheet" href="style.css" />
 <!-- Pour ceux qui ont une résolution inférieure à 1280px -->
<link rel="stylesheet" media="screen and (max-width: 1280px)" href="petite_resolution.css" />
```
- en écrivant la règle directement dans le fichier CSS habituel. Par exemple, si la résolution est inférieure à 1280px de large, charge les propriétés CSS ci-dessous
```css
@media screen and (max-width: 1280px)
{
    /* Rédigez vos propriétés CSS ici */
}
```

----

## Les règles disponibles
Il existe différentes règles permettant de construire des media queries. Voici les principales :
- **color** : gestion de la couleur (en bits/pixel)
- **height** : hauteur de la zone d’affichage (fenêtre)
- **width** : largeur de la zone d’affichage (fenêtre)
- **device-height** : hauteur du périphérique
- **device-width** : largeur du périphérique
- **orientation** : orientation du périphérique (portrait ou paysage)
- **media** : type d’écran de sortie. Quelques valeurs possibles :
  - *screen* : écran classique
  - *handheld* : périphérique mobile
  - *print* : impression
  - *tv* : télévision
  - *projection* : projecteur
  - *all* : tous les types d’écran

On peut ajouter le préfixe **min-** ou **max-** devant la plupart de ces règles. Ainsi **min-width** signifie “largeur minimale”. La différence entre **width** et **device-width** se perçoit surtout sur les navigateurs des smartphones.

Les règles peuvent être combinées à l’aide des mots suivants :
- **only** : uniquement
- **and** : et
- **not** : non

```css
/* Paragraphes en bleu par défaut */
p
{
  color: blue;
}
```

```css
/* Nouvelles règles si la fenêtre fait au maximum 1024px de large */
@media screen and (max-width: 1024px)
{
    p
    {
        color: red;
        background-color: black;
        font-size: 1.2em;
    }
}
```

----

## Mise en pratique des media queries sur le design

Il est intéressant de revoir le design de son site lorsque la résolution est trop faible et qu’il est nécessaire de scroller vers la droite pour voir toute la page.

----

## Media queries et navigateurs mobiles

Les écrans de smartphones sont beaucoup moins larges que nos écran habituels. Pour s’adapter, les navigateurs mobiles affichent le site en dézoomant, ce qui permet d’avoir un aperçu de l’ensemble de la page. La zone d’affichage simulée est appelée le **viewport**. C’est la largeur de la fenêtre du navigateur mobile.
En CSS, avec les media-queries, si vous ciblez l’écran avec max-width sur un mobile, celui-ci va comparer la largeur que vous indiquez avec celle de son viewport. Celui-ci change selon le navigateur mobile : iPhone Safari : 980 pixels, Android : 800 pixels.

Pour cibler les smartphones, plutôt que d’utiliser max-width, il peut être intéressant de recourir à **max-device-width** : c’est la largeur du périphérique. Les périphériques mobiles ne dépassant pas 480 pixels de large, on pourra viser uniquement les navigateurs mobiles avec cette media query.

```css
@media all and (max-device-width: 480px)
{
    /* Vos règles CSS pour les mobiles ici */
}
```

On ne peut pas utiliser **handheld**, car quasiment aucun navigateur mobile ne reconnaît handheld, ils se comportent comme s’ils étaient des écrans normaux (screen).

Pour modifier la largeur du viewport du navigateur mobile, il faut insérer une balise `<meta>` dans l’en-tête (`<head>`)
```html
<meta name="viewport" content="width=320" />
```

Pour obtenir un rendu facile à lire, sans zoom, on peut demander à ce que le viewport soit le même que la largeur de l’écran :
```html
<meta name="viewport" content="width=device-width" />
```
