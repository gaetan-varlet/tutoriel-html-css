# Les inline frames

- `<iframe>` signifie *inline frame*, *cadre en ligne* en français. Il s'insère dans le flot du contenu de la page
- il représente un contexte de navigation imbriqué qui permet en fait d'obtenir une page HTML intégrée dans la page courante
- permet d'intégrer des contenus externes dans notre page, par exemple une vidéo YouTube, une carte Google Maps, ou une autre page HTML
- il faut indiquer le lien ou chemin du document dans l'attribut `src`
- certains sites refusent d'être chargés dans une *iframe*

```html
<iframe src="...">
```