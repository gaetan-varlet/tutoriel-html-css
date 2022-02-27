# Création d’apparences dynamiques

Le CSS permet de modifier l’apparence des éléments de manière dynamique, c’est-à-dire que des éléments peuvent changer de forme une fois que la page a été chargée, grâce à une fonctionnalité puissante du CSS : **les pseudo-formats**.

Possibilité de changer l’apparence :
- au survol
- lors du clic
- lors du focus (élément sélectionné)
- lorsqu’un lien a été consulté

----

## Au survol

Le premier pseudo-format que l’on va manipuler est **:hover**. Comme tous les pseudo-formats que nous allons voir, c’est une information que l’on ajoute après le nom de la balise ou de la classe dans le CSS.

```css
a:hover
{

}
```

`:hover` signifie survoler. Il peut donc se traduire quand la souris est sur le lien.

On peut donc définir l’apparence que doivent avoir les liens lorsqu’on pointe dessus.
```css
a /* Liens par défaut (non survolés) */
{
   text-decoration: none;
   color: red;
   font-style: italic;
}

a:hover /* Apparence au survol des liens */
{
   text-decoration: underline;
   color: green;
}
```

On l’utilise souvent sur les liens mais il est possible de modifier l’apparence de n’importe quel élément comme les paragraphes par exemple lorsqu’on pointe dessus.

----

## Au clic et lors de la sélection

Nous pouvons changer l’apparence des éléments lorsque l’on clique dessus et lorsqu’ils sont sélectionnés.

### `:active` au moment du clic

Le pseudo-format `:active` permet d’appliquer un style particulier au moment du clic. En pratique, il n’est utilisé que sur les liens.
Le lien gardera cette apparence très peu de temps.
On peut par exemple changer la couleur de fond du lien lorsqu’on clique dessus :
```css
a:active /* Quand le visiteur clique sur le lien */
{
    background-color: #FFCC66;
}
```

### `:focus` lorsque l’élément est sélectionné

Le pseudo-format `:focus` applique un style lorsque le l’élément est sélectionné.
Sous Chrome et Safari, l’effet se voit que si l’on appuie sur la touche Tab.
Ce pseudo-format pourra être appliqué à d’autres balises HTML notamment les formulaires.
```css
a:focus /* Quand le visiteur sélectionne le lien */
{
    background-color: #FFCC66;
}
```

----

## Lorsque le lien a déjà été consulté

Il est possible d’appliquer un style à un lien vers une page qui a déjà été vue. Par défaut, le navigateur colore le lien en violet.

Vous pouvez changer cette apparence avec **:visited**. En pratique, sur les liens consultés, on ne peut pas changer beaucoup de choses à part la couleur.
```css
a:visited /* Quand le visiteur a déjà vu la page concernée */
{
    color: #AAA; /* Appliquer une couleur grise */
}
```
Si vous ne souhaitez pas que les liens déjà visités soient colorés d’une façon différente, il vous faudra leur appliquer la même couleur qu’aux liens normaux.
