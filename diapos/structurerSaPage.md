# Structurer sa page

----

Il est conseillé d’utiliser des balises HTML dédiées à la structuration du site. Elles ont été introduites en HTML5 et permettent de distinguer l’en-tête, le menu de navigation, etc…

![Structure d'une page HTML](images/structurePage.png "les différentes sections d'une page HTML")

Les différentes balises :
- `<header>` : en-tête
  - on y trouve souvent un logo, une bannière, le slogan du site…
  - il peut y avoir plusieurs en-têtes dans la page, par exemple un par section
- `<footer>` : pied de page
  - se trouve généralement en bas de la page
  - on y trouve en général des informations comme des liens de contact, le nom de l’auteur, les mentions légales, etc...
- `<nav>` : liens principaux de navigation
  - regroupe les principaux liens de navigation du site. On peut y mettre par exemple le menu principal du site
  - généralement réalisé sous forme de liste à puce à l’intérieur de la balise `<nav>`
- `<section>` : section de page
  - sert à regrouper des contenus en fonction de leur thématique, par exemple une section actualités, une section assistance
  - chaque section peut avoir son titre de niveau 1 (`<h1>`) de même que l’en-tête pour aussi contenir un titre de niveau 1, car chaque bloc est indépendant des autres
- `<aside>` : informations complémentaires
  - il peut y avoir plusieurs blocs `<aside>` dans la page
- `<article>` : article indépendant
  - portion généralement autonome de la page

Ces balises peuvent être imbriquées les unes dans les autres. Par exemple, une section peut avoir sa propre en-tête.
Ces balises ne s’occupent pas de la mise en page, ce sera fait en CSS. Elles servent uniquement à bien structurer la page et à indiquer à l’ordinateur le sens du texte qu’elles contiennent. On pourrait très bien placer l’en-tête en bas de la page si on le souhaite.
