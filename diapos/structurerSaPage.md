# Structurer sa page

Il est conseillé d’utiliser des balises HTML dédiées à la structuration du site. Elles ont été introduites en HTML5 et permettent de distinguer l’en-tête, le menu de navigation, etc…

![Structure d'une page HTML](images/structurePage.png "les différentes sections d'une page HTML")

Les différentes balises :
- `<header>` : en-tête
  - généralement une grande bande placée en travers au haut de la page avec un titre ou un logo
- `<nav>` : liens principaux de navigation
  - regroupe les principaux liens de navigation du site. On peut y mettre par exemple le menu principal du site
  - généralement réalisé sous forme de liste à puce à l’intérieur de la balise `<nav>`
- `<main>` : contenu principal
  - une grande zone au centre contenant la majeure partie du contenu unique de la dite page (partie variable de page en page)
  - peut-être composée de sous-sections comme des `<article>`, `<section>` et `<div>`
  - devrait être directement à la racine de `<body>` et présent une seule fois
- `<aside>` : informations complémentaires sur le côté
  - concerne souvent des informations autour du sujet, liens, citations, annonces...
  - souvent mis à l'intérieur de l'élément main
- `<footer>` : pied de page
  - se trouve généralement en bas de la page
  - on y trouve en général des informations comme des liens de contact, le nom de l’auteur, les mentions légales, etc...
- `<article>` : représente une composition autonome dans un document, par exemple un billet de blog
- `<section>` :
  - ressemble à `<article>`, mais sert plutôt à contenir une partie isolée de la page constituant un élément de fonctionnalité en soi
  - sert à regrouper des contenus en fonction de leur thématique, par exemple une section actualités, une section assistance
  - chaque section commence généralement par un titre

Ces balises peuvent être imbriquées les unes dans les autres. Par exemple, une section peut avoir sa propre en-tête.

Ces balises ne s’occupent pas de la mise en page, ce sera fait en CSS. Elles servent uniquement à bien structurer la page et à indiquer à l’ordinateur le sens du texte qu’elles contiennent. On pourrait très bien placer l’en-tête en bas de la page si on le souhaite.
