# Le modèle des boîtes
Une page web est une succession et un empilement de boîtes, appelés blocs. La plupart des éléments vus au chapitre précédent (header, article, nav…) sont des blocs, comme `<p>`, `<h1>`...
Nous allons apprendre à manipuler ces blocs comme de véritables boîtes, en leur donnant des dimensions, jouer sur leurs marges, gérer leur contenu…

----

## Les balises de type block et inline

La plupart des balises peuvent se ranger dans l’une des deux catégories suivantes :
- **Les balises block** : c’est le cas par exemple des paragraphes `<p></p>`
  - elles créent automatiquement un retour à la ligne avant et après
  - il est possible de mettre un bloc dans un autre bloc
- **Les balises inline** : c’est le cas par exemple des liens `<a></a>`
  - elles se trouvent obligatoirement à l’intérieur d’une balise block
  - elles ne créent pas de retour à la ligne, le texte s’écrit à la suite du texte précédent, c’est pour cela que l’on parle de balise “en ligne”

Il existe plusieurs autres catégories très spécifiques, comme les cellules de tableau ou les puces. Elles sont minoritaires.

**Les balises universelles**
Il s’agit des balises `<span>` (type inline) et `<div>` (type block) qui n’ont aucun sens particulier contrairement à `<p>` par exemple qui veut dire paragraphe.
Elles sont pratiques mais attention de ne pas en abuser.
Exemple d’un span inutile : `<span class=”important”>`, alors qu’il existe `<strong>` qui sert à indiquer l’importance.
Exemple d’un div inutile `<div class=titre>`, alors qu’il existe `<h1>`, `<h2>`...

----

## Les dimensions
Nous travaillerons ici uniquement avec les balises de type block. Contrairement à un inline, un bloc a une largeur et une hauteur :
  - **width** : largeur du bloc, en pixels (50px) ou en pourcentage (95%)
  - **height** : hauteur du bloc en pixels ou pourcentage

Il s’agit précisément de la largeur et de la hauteur du contenu du bloc, auquel peut s’ajouter des marges. Par défaut, un bloc prend 100% de la largeur disponible. Les pourcentages sont utiles pour créer un design qui s’adapte à la résolution d’écran du visiteur. Il faut utiliser les pixels si on a besoin d’un bloc avec une dimension précise.

**Minimum et maximum**
On peut demander à ce qu’un bloc ait des dimensions minimales ou maximales.
Il existe différentes propriétés :
- **min-width** : largeur minimale
- **min-height** : hauteur minimale
- **max-width** : largeur maximale
- **max-height** : hauteur maximale

Par exemple, si on veut que les paragraphes occupent 50 de la largeur avec au moins 400 pixels de large :
```css
p
{
    width: 50%;
    min-width: 400px;
}
```

----

## Les marges
Tous les blocs possèdent des marges. Il existe deux types de marges :
- les marges intérieures
- les marges extérieures

On utilise les propriétés CSS suivantes :
- **padding** pour indiquer la taille des marges intérieures, généralement en pixels (px)
- **margin** pour indiquer la taille des marges extérieures, aussi en pixels

Par défaut, il n’y a pas de marge intérieure, mais il y a une marge extérieure qui fait que deux paragraphes ne sont pas collés et qu’on a l’impression de sauter à la ligne.
Pour ajouter une marge intérieure de 12 pixels aux paragraphes :
```css
p
{
    padding: 12px; /* Marge intérieure de 12px */
}
```

Cela s’applique aux quatres côtés du bloc. Si on souhaite modifier un côté particulier, il faut utiliser les propriétés **margin-top**, **margin-bottom**, **margin-left**, **margin-right**.
On peut aussi indiquer des valeurs différentes pour les quatres côtés dans la super-propriété **margin**
```css
{
  margin : 2px 0 3px 1px; /* haut, droite, bas et gauche */
}
``````


Les balise de type inline possèdent également des marges, on peut donc aussi utiliser ces propriétés sur ce type de balises.

**Centrer les bloc**
Pratique lorsqu’on ne connaît pas la résolution du visiteur.
Pour centrer, il faut donner une largeur au bloc (avec width) et indiquer que l’on veut des marges extérieures automatiques :
```css
{
  margin: auto;
}
```

On peut quand même modifier les marges en haut et en bas, par exemple :
```css
{
  margin: 20px auto 0 auto;
}
```

Il n’est pas possible de centrer verticalement un bloc avec cette technique, seul le centrage horizontal est permis.

----

## Quand ça dépasse
Quand on définit des dimensions précises pour nos blocs, il arrive qu’ils deviennent trop petits pour le texte qu’ils contiennent.
Il existe des propriétés CSS pour contrôler les dépassements et décider quoi faire.
- **overflow** : permet de couper un bloc si le texte dépasse en dessous. Il peut prendre différentes valeurs :
  - *visible* : le texte dépasse des limites et reste visible (par défaut)
  ```css
  {
    overflow: visible;
  }
  ```
  - *hidden* : si le texte dépasse des limites, il sera coupé, on ne pourra pas voir tout le texte
  - *scroll* : le texte sera coupé s’il dépasse des limites mais une barre de défilement sera disponible pour lire l’ensemble du texte
  - *auto* : mode automatique. Le navigateur décide de mettre ou non des barres de défilement seulement si c’est nécessaire. C’est la valeur à utiliser le plus souvent
- **word-wrap** : pour couper les textes trop larges, comme un mot très long qui ne tient pas dans la largeur du bloc. Cette propriété permet de forcer la césure des mots très long comme une URL. Il faut l’utiliser dès qu’un bloc est susceptible de contenir du texte saisi par des utilisateurs.
```css
{
  word-wrap: break-word;
}
 ```
