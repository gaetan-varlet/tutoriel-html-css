# La vidéo et l'audio
Jusqu’à l’arrivée de l’HTML5, aucune balise ne permettait de gérer la vidéo. Il fallait passer par un plugin comme Flash. Avec le HTML5, deux nouvelles balises ont été créées : `<video>` et `<audio>`.

----

## Les formats audio et vidéo

### Les formats audio
- Formats compressés : MP3, AAC (utilisé majoritairement par Apple sur iTunes), OGG (format libre)
- Format non compressé : WAV (à éviter)

### Les formats vidéo
Pour stocker une vidéo, il faut trois éléments :
- **un format conteneur** : un genre de boite qui va servir à contenir les deux autres éléments. On le reconnaît généralement grâce à son extension : AVI, MP4, MKV…
- **un codec audio** : c’est le format du son de la vidéo, généralement compressé (MP3, AAC, OGG…)
- **un codec vidéo** : c’est le format qui va compresser les images. Ces formats sont complexes et on ne peut pas toujours les utiliser gratuitement. Les principaux à connaître pour le web sont :
  - **H.264** : l’un des plus puissants et des plus utilisés mais pas à 100% gratuit. Utilisable gratuitement sur les sites web personnel
  - **Ogg Theora** : codec gratuit et libre de droits mais moins puissant que H.264
  - **WebM** : autre codec gratuit et libre, plus récent. Proposé par Google, c’est le concurrent le plus sérieux de H.264

Il est conseillé de proposer chaque vidéo dans plusieurs formats pour qu’elle soit lisible sur un maximum de navigateurs.

----

## Insertion d’un élément audio
En théorie, il suffit d’une simple balise :

```html
<audio src="musique.mp3"></audio>
```

Dans les faits, avec ce code, rien ne s'affiche à l’écran, le navigateur télécharge seulement les métadonnées du fichier.


Il est possible d’ajouter des attributs :
- **controls** : pour ajouter les boutons Lecture, Pause et la barre de défilement. Elle n’y est pas par défaut car certains site web préfèrent créer eux-mêmes leurs propres boutons et commander la lecture avec du JavaScript.
- **width** : modifier la largeur de l’outil de lecture
- **loop** : la musique sera jouée en boucle
- **autoplay** : la musique sera jouée dès le chargement de la page. A éviter car irritant et peu apprécié.
- **preload** : indique si la musique peut être préchargée dès le chargement de la page. Cet attribut prend les valeurs suivantes :
  - *auto* : le navigateur décide s’il doit précharger  toute la musique, uniquement les métadonnées ou rien du tout (par défaut)
  - *metadata* : charge uniquement les métadonnées (durée, etc…)
  - *none* : pas de préchargement .Utile pour ne pas gaspiller de bande passante
On ne peut pas forcer le préchargement de la musique, c’est toujours le navigateur qui décide.

Il est conseillé d’écrire un message entre les balises pour les navigateurs qui ne comprennent pas la balise, qui sera affiché à la place du lecteur le cas échéant. Sinon, il ne sera pas affiché.

```html
<audio src="hype_home.mp3" controls>Veuillez mettre à jour votre navigateur !</audio>
```

Il faut proposer plusieurs versions du fichier audio pour assurer une compatibilité avec un maximum de navigateur. Le navigateur prendra automatiquement le format qu’il reconnaît.
```html
<audio controls>
    <source src="hype_home.mp3">
    <source src="hype_home.ogg">
</audio>
```

----

## Insertion d’une vidéo
Il suffit d’une simple balise `<video>` pour insérer une vidéo dans la page.

```html
<video src="sintel.webm"></video>
```

Dans cet exemple, aucun contrôle ne permet de lancer la vidéo.
Ajoutons quelques attributs (la plupart sont les mêmes que pour la balise `<audio>`) :
- **poster** : image à afficher à la place de la vidéo tant qu’elle n’est pas lancée. Par défaut, le navigateur prend la première image de la vidéo
- **controls** : pour ajouter Lecture, etc… comme pour l’audio
- **width** : pour modifier la largeur de la vidéo
- **height** : pour modifier la hauteur de la vidéo
- **loop** : la vidéo sera jouée en boucle
- **autoplay** : vidéo jouée dès le chargement
- **preload** : indique si la vidéo peut être préchargée dès le chargement
  - *auto* : le navigateur décide s’il doit précharger toute la vidéo, uniquement les métadonnées ou rien du tout (par défaut)
  - *metadata* : charge les métadonnées (durée, dimensions…)
  - *none* : pas de préchargement
On ne peut pas forcer le préchargement de la vidéo, c’est toujours le navigateur qui décide.

Les proportions de la vidéo sont toujours conservées. Si vous définissez une largeur et une hauteur, le navigateur fera en sorte de ne pas dépasser les dimensions indiquées mais il conservera les proportions.

```html
<video src="sintel.webm" controls poster="sintel.jpg" width="600">
    Il est temps de mettre à jour votre navigateur !
</video>
```

Comme pour l’audio, il est conseillé d’afficher un message entre les balises vidéo pour les navigateurs ne supportant pas ces balises.

Pour contenter tous les navigateurs, on va utiliser la balise `<source>` à l’intérieur de la balise `<video>` pour proposer différents formats.

Il n’y pas de moyen de forcer le plein écran, même en JavaScript. Ce n’est pas non plus possible de protéger la vidéo contre le téléchargement. Les lecteurs vidéos Flash permettent de protéger le contenu des vidéos mais des solutions de contournement existent.
