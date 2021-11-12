# Les div et les span

----

Ce sont des balises qui n'ont pas de sens particulier d'un point de vue sémentique, elles sont dites universelles
- `<div>` est un balise HTML conteneur, utilisé pour groupes d'autres éléments
	- c'est une balise de type **block**, qui entoure un bloc de texte, comme les balises `<p>` et `<h1>`. Ces balises créent un nouveau bloc dans la page et provoque donc un retour à la ligne
	- utilise pour appliquer un style (via *class* ou *id*) ou une langue par exemple
	- à utiliser uniquement si aucun autre élément sémantique (`<article>` ou `<nav>` par exemple) n'est approprié
- `<span>` est l'équivalent de la `div` mais est de type **inline**, c’est-à-dire que l’on place au sein d’un paragraphe de texte pour sélectionner certains mots uniquement, comme les balises `<strong>` et `<em>`
