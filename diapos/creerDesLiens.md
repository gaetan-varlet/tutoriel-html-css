# Créer des liens

Les liens permettent d'aller d’une page à une autre

----

## Un lien vers un autre site
Il faut utiliser la balise `<a>` avec un attribut `href` pour indiquer vers quelle page le lien doit conduire. Par exemple, le code ci-dessous amène vers OpenClassrooms :
```html
<a href="https://openclassrooms.com">OpenClassrooms</a>
```

Par défaut, le lien s’affiche en bleu et en violet si la page a déjà été ouverte. Nous verrons comment changer cette apparence lorsque nous étudierons le CSS.

Ces liens s’appellent **liens absolus** car ils indiquent l’adresse complète. Il existe des liens différents qui permettent de faire le lien entre les pages de notre site.

----

## Un lien vers une autre page de son site
On parle de lien relatif.

Pour aller sur la page 2, si le fichier html est dans le même dossier que la page 1, alors il faut utiliser le code suivant :
```html
<p>Bonjour. Souhaitez-vous consulter <a href="page2.html">la page 2</a> ?</p>
```

**Deux pages situées dans des dossiers différents**
Si page2 se trouve dans un sous-dossier appelé contenu :
```html
<a href="contenu/page2.html">
  ```

Si c’est dans un dossier parent :
```html
<a href="../page2.html">
```

----

## Un lien vers une ancre
Une ancre est un point de repère que l’on met dans une page HTML lorsqu’elle est longue. Il peut être utile de faire un lien amenant plus bas dans la page.
Pour créer une ancre, il suffit de rajouter l’attribut id à une balise qui va servir de repère.
Ensuite, il faut créer un lien avec un `#` dans l’attribut href.
```html
<h2 id="mon_ancre">Titre</h2>
<a href="#mon_ancre">Aller vers l'ancre</a>
```

L’attribut `id` sert à donner un nom unique à une balise pour s’en servir de repère. Cet attribut servira en CSS pour repérer une balise précise.

**Liens vers une ancre situé dans une autre page**
L’idée est de faire un lien qui ouvre une autre page et amène directement à une ancre située plus bas sur cette page.
Par exemple, pour aller sur la page ancres.html au niveau de l’ancre rollers :
```html
<a href="ancres.html#rollers">
```

----

## Cas pratique d’utilisation des liens

### Un lien qui affiche une infobulle
L’attribut `title` affiche une bulle d’aide lorsqu’on pointe sur le lien. Attribut facultatif.
```html
<p>Bonjour. Souhaitez-vous visiter <a href="https://openclassrooms.com" title="Vous ne le regretterez pas !">OpenClassrooms</a> ?</p>
```

### Un lien qui ouvre une nouvelle fenêtre
Il est possible de forcer l’ouverture d’un lien dans une nouvelle fenêtre en ajoutant `target=”_blank”`. Déconseillé car perturbe la navigation. De plus l’utilisateur peut décider de le faire lui même avec des commandes clavier.
```html
<p>Bonjour. Souhaitez-vous visiter <a href="https://openclassrooms.com" title="Vous ne le regretterez pas !" target="_blank">OpenClassrooms</a> ?</p>
```

### Un lien pour envoyer un e-mail
Il faut utiliser des liens de type `mailto:` et écrire le mail où on peut nous contacter.
```html
<p><a href="mailto:votrenom@bidule.com">Envoyez-moi un e-mail !</a></p>
```

### Un lien pour télécharger un fichier
Il s’agit d’un lien comme pour accéder à une page web mais en indiquer le nom du fichier à télécharger. Le navigateur voyant qu’il ne s’agit pas d’une page web à afficher va lancer la procédure de téléchargement lorsqu’on cliquera sur le lien.
```html
<p><a href="monfichier.zip">Télécharger le fichier</a></p>
```
