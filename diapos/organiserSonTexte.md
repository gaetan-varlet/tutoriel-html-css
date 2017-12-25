# Organiser son texte

----

## Organiser son texte

### Les paragraphes

La plupart du temps, on écrit du texte à l’intérieur d’un paragraphe.
```html
<p>Bonjour et bienvenue sur mon site !</p>
```

**Sauter une ligne**
Passer à la ligne dans l’éditeur de texte ne fait pas passer à la ligne à l’affichage dans le navigateur.
Il est possible d’écrire un deuxième paragraphe pour aller à la ligne.
```html
<p> </p>
```
Il est aussi possible d’utiliser une balise orpheline à l’intérieur d’un paragraphe pour aller à la ligne :
```html
<br />
```

----

## Les titres
Il y a 6 niveau de titres en HTML de très important à moins important :
```html
<h1> </h1> <!-- titre très important, en général pour afficher le titre de la page au début de celle-ci -->
<h6> </h6>
```
En général, 3 niveaux de titres suffisent.  
Il ne faut pas choisir la balise en fonction de la taille qu’elle applique, il faut impérativement commencer par h1 puis h2. La taille du texte se modifie en CSS. Grâce au langage CSS, nous pourrons dire que je veux que mes titres h1 soient centrés, rouges et soulignés.
**Le langage HTML sert uniquement à rédiger le contenu de la page, la mise en forme se fera avec le langage CSS.**

----

## La mise en valeur
mettre un peu valeur : encadrer les mots avec les balises `em`
```html
<em> </em>
```
Le texte est mis en italique. C’est le navigateur qui choisit cela.

Mettre bien en valeur : encadrer les mots avec les balises `strong`
```html
<strong> </strong>
```
Le texte s’affiche en gras, toujours un choix du navigateur. La balise strong ne signifie pas mettre en gras mais important. En CSS, on pourra décider d’afficher les mots importants d’une autre façon.

Marquer le texte : permet de faire ressortir visuellement une portion de texte pas forcément considéré comme important avec les balises `mark`. Par défaut, mark a pour effet de surligner le texte.
```html
<mark> </mark>
```

**Ne pas oublier HTML pour le fond, CSS pour la forme**
Les balises de mise en valeur ne servent pas à dire que le texte apparaîtra en gras, en italique ou souligné mais que le texte est important.

----

## Les listes
Les listes permettent de mieux structurer notre texte et d’ordonner nos informations. Nous allons découvrir deux types de listes :
- les listes non ordonnées ou listes à puces
- les listes ordonnées ou listes numérotées ou encore énumérations

### Liste non ordonnée
C’est une liste sans notion d’ordre. Il est possible de faire des listes dans les listes.

exemple :
- Fraises
- Framboises
- Cerises
```html
<ul>
    <li>Fraises</li>
    <li>Framboises</li>
    <li>Cerises</li>
</ul>
```

### Liste ordonnée
Une liste ordonnée fonctionne de la même façon, il faut juste remplacer `<ul></ul>` par `<ol></ol>`.
```html
<ol>
    <li>Je me lève.</li>
    <li>Je mange et je bois.</li>
    <li>Je retourne me coucher.</li>
</ol>
```
1. Je me lève.
2. Je mange et je bois.
3. Je retourne me coucher.

Pour information, il existe un troisième type de liste beaucoup plus rare : la liste de définition avec les balises `<dl>` `<dt>` et `<dd>`.
