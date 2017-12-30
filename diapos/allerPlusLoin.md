# Aller plus loin

---

## Du site web à l’application web
JavaScript permet de rendre une page plus interactive :
- modifier des propriétés CSS sans recharger la page
- modifier le code source HTML sans avoir à recharger la page, pendant que le visiteur consulte la page
- permet d’afficher des boîtes de dialogue à l’écran du visiteur
- modifier la taille de la fenêtre

JavaScript est régulièrement utilisé pour faire de l’AJAX (échanges de données entre la page et le serveur). Cela permet de modifier une partie de la page web que le visiteur consulte en échangeant des données avec le serveur. Cela donne l’impression que la page est plus dynamique et réactive.

----

## Technologie liées à HTML5
LE W3C ne travaille pas que sur le HTML et le CSS, mais cherche aussi à les compléter.
Voici quelques technologies introduites en parallèle de HTML5 :
- **Canvas** : permet de dessiner au sein de la page web à l’intérieur de la balise HTML `<canvas>`
- **SVG** : permet de créer des dessins vectoriels, qui peuvent être agrandis à l’infini
- **Drag & Drop** : permet de faire glisser-déposer des objets dans la page web
- **File API** : permet d’accéder aux fichiers stockés sur la machine du visiteur avec son autorisation
- **Géolocalisation** : pour localiser le visiteur
- **Web Storage** : permet de stocker un grand nombre d’informations sur la machine du visiteur, alternative plus puissante aux traditionnels cookies
- **Appcache** : permet de demander au navigateur de mettre en cache certains fichiers pour ne plus les télécharger systématiquement
- **Web Sockets** : permet des échanges plus rapides, en temps réel, entre le navigateur et le serveur qui gère le site web (une sorte d’AJAX). C’est l’avenir des applis web
- **WebGL** : permet d’introduire de la 3D dans les pages web

La plupart de ces technologies s’utilisent avec JavaScript, il s’agit donc de nouvelles fonctionnalités que l’on peut utiliser en JavaScript.

----

## Les sites web dynamiques
Les langages dont nous allons parler ici sont des langages de programmation comme JavaScript, sauf que JavaScript s’exécute sur la machine des visiteurs tandis que les langages que nous allons voir s’exécute sur le serveur qui contient le site web.

Il y a davantage de contrôles à programmer côté serveur qu'en JavaScript mais certaines actions ne peuvent être réalisées que côté navigateur.

Les langages serveur permettent de générer la page web lorsque le visiteur arrive sur le site. Chaque visiteur peut donc obtenir une page web personnalisée.

Les langages ne servent pas au même chose, ils se complètent. En utilisant HTML + CSS + JavaScript + PHP, vous pouvez faire de l’AJAX, effectuer des calculs, stocker des informations dans des bases de données… bref des vrais sites web dynamiques.

Les langages côté serveur sont nombreux, en voici quelques-uns :
- **PHP** : facile à utiliser et puissant
- **Java EE** (Java) : très utilisé dans le monde professionnel. c’est une extension du langage Java. Un peu plus compliqué à prendre en main que PHP
- **ASP.NET**
- **Django** (Python)
- **Ruby on Rails** (Ruby)

Connaître l’un de ces langages est indispensable pour traiter le résultat des formulaires HTML.
