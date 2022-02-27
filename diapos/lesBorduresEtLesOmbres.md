# Les bordures et les ombres

## Bordures standard

- Il existe de nombreuses propriétés CSS : **border-width**, **border-color**, **border-style**…
- Il est aussi possible d’utiliser la super propriété **border** qui regroupe l’ensemble de ces propriétés.

On peut utiliser jusqu’à trois valeurs pour modifier l’apparence de la bordure :
- **la largeur** : largeur de la bordure, en pixels, comme 2px
- **la couleur** : couleur de la bordure, soit un nom de couleur (black, red…), soit une valeur hexadécimale (`#FF0000`), soit une valeur RGB
- **le type de bordure** : il existe différents types de bordures
  - *none* : pas de bordure (par défaut)
  - *solid* : trait simple
  - *dotted* : pointillés
  - *dashed* : tirets
  - *double* : bordure double
  - *groove* : en relief
  - *ridge* : autre effet relief
  - *inset* : effet 3D global enfoncé
  - *outset* : effet 3D global surélevé

  Il est également possible d’avoir des bordures différentes selon le côté avec les propriétés suivantes : **border-top**, **border-bottom**, **border-left**, **border-right**.
  Ce sont aussi des super-propriétés, elles fonctionnent comme border mais ne s'appliquent qu’à un seul côté.

  Si l’on souhaite uniquement une bordure à gauche et à droite sur un élément, il faut donc utiliser les propriétés border-left et border-right.

  Il est possible de modifier les bordures des paragraphes mais aussi de n’importe quel type d’éléments comme les images, les textes importants comme `<strong>`, etc...

----

## Bordures arrondies

- Les bordures arrondies sont facilement utilisable avec le CSS3.
- La propriété **border-radius** va nous permettre d’arrondir facilement les angles de n’importe quel élément.
- Il suffit d’indiquer la taille de l’arrondi en pixels. L’arrondi se voit si l’élément a des bordures ou à une couleur de fond.

```css
p
{
    border-radius: 10px;
}
```

On peut aussi préciser la forme de l’arrondi de chaque coin. L’ordre est haut-gauche, haut-droit, bas-droit, bas-gauche.
```css
p
{
    border-radius: 10px 5px 10px 5px;
}
```

Il est aussi possible d’affiner l’arrondi des angles en créant des courbes elliptiques. Il faut indiquer deux valeurs séparées par une barre oblique.
```css
p
{
    border-radius: 20px / 10px;
}
```

----

## Les ombres

C’est une nouveauté CSS3. Nous allons voir les ombres des boîtes et les ombres du texte.

### box-shadow : les ombres des boîtes
La propriété **box-shadow** s’applique à tout le bloc et prend quatre valeurs dans l’ordre suivant :
1. le décalage horizontale de l’ombre
2. le décalage verticale de l’ombre
3. l’adoucissement du dégradé
4. la couleur de l’ombre

Par exemple, pour une ombre noir sans adoucissement, on écrira :
```css
p
{
    box-shadow: 6px 6px 0px black;
}
```

On peut ajouter une cinquième valeur facultative : **inset**. Dans ce cas, l’ombre sera placée à l’intérieur du bloc, pour donner un effet enfoncé.


### text-shadow : l’ombre du texte
Avec la propriété **text-shadow**, il est possible d’ajouter une ombre directement sur les lettres du texte. Les valeurs fonctionnent exactement de la même façon que box-shadow.
```css
p
{
    text-shadow: 2px 2px 4px black;
}
```
