# Formatage du texte
On va apprendre à modifier l’apparence du texte, on dit qu’on le met en forme.

----

## La taille
Pour modifier, la taille, on utilise la propriété CSS **font-size**.
- indiquer une taille absolue : en pixels (px), en centimètres (cm) ou millimètres (mm). Très précis mais à éviter car risque d’indiquer une taille trop petite pour certains lecteurs.
```css
 {font-size: 16px;}
```
- indiquer une taille relative : en pourcentage, “em” ou “ex”. Technique plus souple qui a l’avantage de s’adapter facilement aux préférences de taille des visiteurs.  
Valeur prédéfini : xx-small, x-small, small, medium, large, x-large, xx-large
```css
{font-size: small}
```
- indiquer la taille en em. (taille normale égal à 1em)
```css
{font-size: 1.3em;}
```

----

## La police
Pour qu’une police s’affiche, il faut que l’internaute l’ait, sinon le navigateur prendra une police par défaut. Depuis CSS3, il est possible de faire télécharger automatiquement une police au navigateur.
Pour indiquer la police à utiliser, il faut utiliser la propriété **font-family**. Il est possible d’indiquer plusieurs noms de police pour éviter si l’internaute n’a pas la même police que vous. Le navigateur essaiera d’abord d’utiliser la police1 puis la police2…
En général, on indique en tout dernier serif qui correspond à une police par défaut. Il existe aussi une police par défaut appelé sans-serif qui n’a pas de petites pattes de liaisons en bas des lettres.
```css
balise
{
    font-family: police1, police2, police3, police4;
}
```

Les polices les plus courantes sont : Arial, Arial Black, Comic Sans MS, Courier New, Georgia, Impact, Times New Roman, Trebuchet MS, Verdana.

Il est possible d’utiliser une police personnalisée avec `@font-face`.

----

## Italique, gras, souligné

### Mettre en italique
La balise `<em>` sert à mettre en valeur un mot mais pas à le mettre en italique. La plupart des navigateurs font cela mais ce n’est pas une obligation.
Le CSS lui, permet de dire réellement je veux que ce texte soit en italique.
On utilise la propriété **font-style** qui peut prendre trois valeurs :
- *italic* : texte en italique
- *oblique* : texte en oblique (légèrement différent de l’italique)
- *normal* : texte normal (par défaut). Cela permet d’annuler une mise en italique car par exemple si on ne veut pas que les textes entre <em> ne soient pas en italique.

### Mettre en gras
Encore une fois, ce n’est pas `<strong>` qui permet de mettre en gras.
La propriété CSS pour mettre en gras est **font-weight** et prend les valeurs suivantes :
- *bold* : texte en gras
- *normal* : texte normal (par défaut)

### Soulignement et autres décorations
La propriété CSS associée porte bien son nom : **text-decoration**. Voici ces différentes valeurs :
- *underline* : souligné
- *line-through* : barré
- *overline* : ligne au-dessus
- *blink* : clignotant (ne fonctionne pas sur tous les navigateurs)
- *none* : normal (par défaut)

### L’alignement
Le langage CSS permet de faire tous les alignements connus. On utilise la propriété **text-align**. Les valeurs sont les suivantes :
- *left* : par défaut
- *center*
- *right*
- *justify*

Il n’est pas possible de modifier l’alignement du texte d’une balise inline (comme `<span>, <a>, <em>, <strong>...`). L’alignement ne fonctionne que sur des balises de type block (`<p>, <div>, <h1>...`) et c’est logique car on ne peut pas modifier l’alignement de quelques mots au milieu d’un paragraphe.

### Les flottants
Le CSS permet de faire flotter un élément autour du texte. On dit aussi qu’on fait un habillage. La propriété est float, elle prend 2 valeurs : *left* et *right*.
On peut utiliser la propriété aussi bien sur des balises block que sur des balises inline. Il est courant de faire flotter une image pour qu’elle soit habillée par du texte.

Il faut par exemple mettre une image dans un paragraphe et ensuite faire flotter cette image en CSS.
```html
<p><img src="flash.gif" class="imageflottante" alt="Image flottante" />
  Ceci est un texte normal de paragraphe, écrit à la suite de l'image
  et qui l'habillera car l'image est flottante.</p>
```
```css
.imageflottante
{
    float: left;
}
```

**Stopper un flottant**
Pour faire continuer le texte en dessous d’un flottant et non à côté, il faut utiliser la propriété **clear** qui peut prendre trois valeurs :
- *left* : le texte se poursuit en-dessous après un `float: left;`
- *right* : le texte se poursuit en-dessous après un `float: right;`
- *both* : le texte se poursuit en-dessous que ce soit après un `float: left;` ou après un `float: right;`
Il est donc plus simple de tout le temps utiliser un `clear: both;`.

```html
<p><img src="flash.gif" class="imageflottante" alt="Image flottante" /></p>
<p>Ce texte est écrit à côté de l'image flottante.</p>
<p class="dessous">Ce texte est écrit sous l'image flottante.</p>
```
```css
.imageflottante
{
    float: left;
}
.dessous
{
    clear: both;
}
```
