---
title: grid-template
slug: Web/CSS/grid-template
---

{{CSSRef}}

La propriété **`grid-template`** est une [propriété raccourcie](/fr/docs/Web/CSS/Shorthand_properties) permettant de définir les colonnes, grilles et zones d'une grille.

{{InteractiveExample("CSS Demo: grid-template")}}

```css interactive-example-choice
grid-template:
  "a a a" 40px
  "b c c" 40px
  "b c c" 40px / 1fr 1fr 1fr;
```

```css interactive-example-choice
grid-template:
  "b b a" auto
  "b b c" 2ch
  "b b c" 1em / 20% 20px 1fr;
```

```css interactive-example-choice
grid-template:
  "a a ." minmax(50px, auto)
  "a a ." 80px
  "b b c" auto / 2em 3em auto;
```

```html interactive-example
<section class="default-example" id="default-example">
  <div class="example-container">
    <div class="transition-all" id="example-element">
      <div>One</div>
      <div>Two</div>
      <div>Three</div>
    </div>
  </div>
</section>
```

```css interactive-example
#example-element {
  border: 1px solid #c5c5c5;
  display: grid;
  grid-gap: 10px;
  width: 200px;
}

#example-element :nth-child(1) {
  background-color: rgba(0, 0, 255, 0.2);
  border: 3px solid blue;
  grid-area: a;
}

#example-element :nth-child(2) {
  background-color: rgba(255, 0, 200, 0.2);
  border: 3px solid rebeccapurple;
  grid-area: b;
}

#example-element :nth-child(3) {
  background-color: rgba(94, 255, 0, 0.2);
  border: 3px solid green;
  grid-area: c;
}
```

Les propriétés détaillées sont {{cssxref("grid-template-rows")}}, {{cssxref("grid-template-columns")}} et {{cssxref("grid-template-areas")}}.

## Syntaxe

```css
/* Valeur avec un mot-clé */
grid-template: none;

/* Valeurs utilisant grid-template-rows / grid-template-columns */
grid-template: 100px 1fr / 50px 1fr;
grid-template: auto 1fr / auto 1fr auto;
grid-template: [linename] 100px / [columnname1] 30% [columnname2] 70%;
grid-template: fit-content(100px) / fit-content(40%);

/* Valeurs utilisant grid-template-areas grid-template-rows / grid-template-column */
grid-template:
  "a a a"
  "b b b";
grid-template:
  "a a a" 20%
  "b b b" auto;
grid-template:
  [header-top] "a a a" [header-bottom]
  [main-top] "b b b" 1fr [main-bottom]
  / auto 1fr auto;

/* Valeurs globales */
grid-template: inherit;
grid-template: initial;
grid-template: unset;
```

### Valeurs

- `none`
  - : Un mot-clé qui applique `none` sur les trois propriétés détaillées et qui indique qu'il n'y a pas de grille explicite. Il n'y a pas de zone de grille nommée. Les lignes et les colonnes seront générées de façon implicite et leurs tailles seront déterminées par les propriétés {{cssxref("grid-auto-rows")}} et {{cssxref("grid-auto-columns")}}.
- `<'grid-template-rows'> / <'grid-template-columns'>`
  - : Voir {{cssxref("grid-template-rows")}} et {{cssxref("grid-template-columns")}} pour les valeurs définies. {{cssxref("grid-template-areas")}} recevra la valeur `none`.
- `[ <line-names>? <string> <track-size>? <line-names>? ]+ [ / <track-list> ]?`
  - : {{cssxref("grid-template-areas")}} est définie avec les chaînes listées, {{cssxref("grid-template-rows")}} est définie avec les tailles de piste suivant chaque chaîne (`auto` sera utilisé pour les tailles manquantes), les lignes seront découpées selon les noms avant et après chaque taille. {{cssxref("grid-template-columns")}} sera définie avec la valeur listée après la barre oblique (ou `none` sinon).

    > [!NOTE]
    > La fonction {{cssxref("repeat()")}} n'est pas autorisée parmi les listes de pistes car les pistes sont conçues pour correspondre à la disposition finale (à la façon d'un dessin en ASCII).

> [!NOTE]
> La propriété raccourcie {{cssxref("grid")}} accepte la même syntaxe mais réinitialise également les propriétés implicites avec leurs valeurs initiales. On pourra utiliser `grid` (plutôt que `grid-template`) pour empêcher les valeurs de suivre la cascade de façon séparée.

## Définition formelle

{{CSSInfo}}

## Syntaxe formelle

{{CSSSyntax}}

## Exemples

### CSS

```css
#page {
  display: grid;
  width: 100%;
  height: 200px;
  grid-template:
    [header-left] "head head" 30px [header-right]
    [main-left] "nav main" 1fr [main-right]
    [footer-left] "nav foot" 30px [footer-right]
    / 120px 1fr;
}

header {
  background-color: lime;
  grid-area: head;
}

nav {
  background-color: lightblue;
  grid-area: nav;
}

main {
  background-color: yellow;
  grid-area: main;
}

footer {
  background-color: red;
  grid-column: foot;
}
```

### HTML

```html
<section id="page">
  <header>En-tête</header>
  <nav>Navigation</nav>
  <main>Zone principale</main>
  <footer>Bas de page</footer>
</section>
```

### Résultat

{{EmbedLiveSample("Exemples", "100%", "200px")}}

## Spécifications

{{Specifications}}

## Compatibilité des navigateurs

{{Compat}}

## Voir aussi

- {{cssxref("grid-template-rows")}}
- {{cssxref("grid-template-areas")}}
- {{cssxref("grid-template-columns")}}
- [Guide : Placer les éléments d'une grille sur les lignes](/fr/docs/Web/CSS/CSS_grid_layout/Grid_layout_using_line-based_placement)
- [Guide : Les zones de grilles et les propriétés raccourcies](/fr/docs/Web/CSS/CSS_grid_layout/Grid_template_areas#les_propri%c3%a9t%c3%a9s_raccourcies_pour_les_grilles_css)
- Tutoriel vidéo : [les propriétés raccourcies pour les zones de grille (en anglais)](https://gridbyexample.com/video/grid-template-shorthand/)
