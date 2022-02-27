# Organiser son texte

----

## Les paragraphes

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
<br /> <!-- forme historique -->
<br>
```

----

## Les titres

Il y a 6 niveau de titres en HTML de très important à moins important :
```html
<h1> </h1> <!-- titre très important, en général pour afficher le titre de la page au début de celle-ci -->
<h6> </h6>
```

- en général, 3 niveaux de titres suffisent
- il ne faut pas choisir la balise en fonction de la taille qu’elle applique, il faut impérativement commencer par h1 puis h2. La taille du texte se modifie en CSS. Grâce au langage CSS, nous pourrons dire que je veux que mes titres h1 soient centrés, rouges et soulignés
- **le langage HTML sert uniquement à rédiger le contenu de la page, la mise en forme se fera avec le langage CSS**

----

## La mise en valeur

**Mettre un peu en valeur** 
- encadrer les mots avec les balises `em`
- le texte est mis en italique. C’est le navigateur qui choisit cela

```html
<em> </em>
```

**Mettre bien en valeur**
- encadrer les mots avec les balises `strong`
- le texte s’affiche en gras, toujours un choix du navigateur
- la balise strong ne signifie pas mettre en gras mais important. En CSS, on pourra décider d’afficher les mots importants d’une autre façon

```html
<strong> </strong>
```

**Marquer le texte**
- permet de faire ressortir visuellement une portion de texte pas forcément considéré comme important avec les balises `mark`
- par défaut, `mark` a pour effet de surligner le texte

```html
<mark> </mark>
```

**Ne pas oublier HTML pour le fond, CSS pour la forme** : les balises de mise en valeur ne servent pas à dire que le texte apparaîtra en gras, en italique ou souligné mais que le texte est important.

----

## Les listes

Les listes permettent de mieux structurer notre texte et d’ordonner nos informations. Il existe 3 types de liste :
- les listes non ordonnées ou listes à puces
- les listes ordonnées ou listes numérotées ou encore énumérations
- les listes de descriptions

### Liste non ordonnée

C’est une liste sans notion d’ordre. Il est possible de faire des listes dans les listes.

```html
<ul>
    <li>Fraises</li>
    <li>Framboises</li>
    <li>Cerises</li>
</ul>
```

- Fraises
- Framboises
- Cerises

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

### Liste de descriptions

La liste de description/définition avec les balises `<dl>`, `<dt>` et `<dd>`.

```html
<dl>
  <dt>Coffee</dt>
  <dd>Black hot drink</dd>

  <dt>Milk</dt>
  <dd>White cold drink</dd>
</dl>
```

### Les entités

Certains caractères spéciaux sont réservés pour une utilisation en HTML, ils seront analysés en tant que code HTML : `&`, `<`, `>` `"`.

Pour afficher ces caractères comme du texte, il faut les remplacer par l'entité du caractère correspondant :
- `&` = `&amp;`
- `<` = `&lt;`
- `>` = `&gt;`
- `"` = `&quot;`
- espace insécable (permet de cumuler des espaces) = `&nbsp;`

### Autres balises

- la balise `<pre>` représente du texte préformaté, comme des formules mathématiques. Les espaces et les sauts de lignes sont conservés
- la balise `<hr>` permet de faire un séparateur horizontal
- la balise `<blockquote>` permet de définir une citation
- la balise `<sup>` permet de mettre en exposant
- la balise `<code>` représente un fragment de code machine
