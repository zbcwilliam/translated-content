---
title: grid-column-end
slug: Web/CSS/grid-column-end
---

{{CSSRef}}

La propriété **`grid-column-end`** définit la position de la fin d'un élément de la grille dans une zone donnée ou sur un fragment de colonne donné.

{{InteractiveExample("CSS Demo: grid-column-end")}}

```css interactive-example-choice
grid-column-end: auto;
```

```css interactive-example-choice
grid-column-end: 3;
```

```css interactive-example-choice
grid-column-end: -1;
```

```css interactive-example-choice
grid-column-end: span 3;
```

```html interactive-example
<section class="default-example" id="default-example">
  <div class="example-container">
    <div class="transition-all" id="example-element">One</div>
    <div>Two</div>
    <div>Three</div>
  </div>
</section>
```

```css interactive-example
.example-container {
  border: 1px solid #c5c5c5;
  display: grid;
  grid-template-columns: 1fr 1.5fr 1fr;
  grid-template-rows: repeat(3, minmax(40px, auto));
  grid-gap: 10px;
  width: 200px;
}

.example-container > div {
  background-color: rgba(0, 0, 255, 0.2);
  border: 3px solid blue;
}

#example-element {
  background-color: rgba(255, 0, 200, 0.2);
  border: 3px solid rebeccapurple;
}
```

## Syntaxe

```css
/* Valeur avec un mot-clé */
grid-column-end: auto;

/* Valers <custom-ident> */
grid-column-end: somegridarea;

/* Valeurs <integer> + <custom-ident> */
grid-column-end: 2;
grid-column-end: somegridarea 4;

/* Valeurs span + <integer> + <custom-ident> */
grid-column-end: span 3;
grid-column-end: span somegridarea;
grid-column-end: 5 somegridarea span;

/* Valeurs globales */
grid-column-end: inherit;
grid-column-end: initial;
grid-column-end: unset;
```

### Valeurs

- `auto`
  - : Un mot-clé qui indique que la propriété ne contribue pas au placement de l'objet sur la grille. Par défaut, la taille du fragment allouée vaut `1` s'il n'y a pas d'autres contraintes.
- `<custom-ident>`
  - : S'il existe une ligne nommée '\<custom-ident>-end', cela placera l'élément sur la première ligne correspondante..

    > [!NOTE]
    > Les noms de zones génèrent automatiquement les noms de colonnes sous cette forme. Ainsi, `grid-column-end: foo;` permettra de désigner l'extrêmité (à la fin) de la zone nommée (sauf si une autre colonne a explicitement été nommée avec `foo-end`).

    Si aucune zone ne correspond, la valeur est traitée comme la combinaison de l'entier 1 et de `<custom-ident>` (cf. définition suivante).

- `<integer> && <custom-ident>?`
  - : Contribue au placement de l'élément sur la n-ième ligne. Si une valeur négative est fournie, les lignes correspondantes sont comptées depuis la dernière. Si un nom est fourni pour \<custom-ident>, seules les lignes avec ce nom sont comptées. S'il n'y a pas suffisamment de lignes avec ce nom, on considère que toutes les lignes sont intitulées avec ce nom afin de trouver une position.

    Un entier nul ne peut pas être utilisé (la règle est invalide).

- `span && [ <integer> || <custom-ident> ]`
  - : Un fragment de grille est utilisé pour le placement de l'élément sur la grille afin que la fin de la colonne pour l'élément de la grille soit placé à n lignes du bord situé au début.

    Si un nom fourni pour \<custom-ident>, seules les lignes ayant ce nom seront comptées. S'il n'y a pas suffisamment de lignes existantes avec ce nom, tout les lignes implicites du côté de la grille explicite et qui correspondent à la direction de la recherche seront comptées afin de placer ce fragment.

    Si \<integer> est absent, la valeur par défaut sera 1. Les entiers négatifs ou nuls ne sont pas autorisés.

    `<custom-ident>` ne peut pas prendre la valeur `span`.

## Définition formelle

{{CSSInfo}}

## Syntaxe formelle

{{CSSSyntax}}

## Exemples

```html
<div class="wrapper">
  <div class="box1">One</div>
  <div class="box2">Two</div>
  <div class="box3">Three</div>
  <div class="box4">Four</div>
  <div class="box5">Five</div>
</div>
```

```css
.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 100px;
}

.box1 {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start: 1;
  grid-row-end: 3;
}

.box2 {
  grid-column-start: 1;
  grid-row-start: 3;
  grid-row-end: 5;
}
```

```css hidden
* {
  box-sizing: border-box;
}

.wrapper {
  border: 2px solid #f76707;
  border-radius: 5px;
  background-color: #fff4e6;
}

.wrapper > div {
  border: 2px solid #ffa94d;
  border-radius: 5px;
  background-color: #ffd8a8;
  padding: 1em;
  color: #d9480f;
}

.nested {
  border: 2px solid #ffec99;
  border-radius: 5px;
  background-color: #fff9db;
  padding: 1em;
}
```

{{EmbedLiveSample('Exemples', '230', '420')}}

## Spécifications

{{Specifications}}

## Compatibilité des navigateurs

{{Compat}}

## Voir aussi

- {{cssxref("grid-column-start")}}
- {{cssxref("grid-column")}}
- {{cssxref("grid-row-start")}}
- {{cssxref("grid-row-end")}}
- {{cssxref("grid-row")}}
- [Guide : le placement sur les lignes d'une grille](/fr/docs/Web/CSS/CSS_grid_layout/Grid_layout_using_line-based_placement)
- Tutoriel vidéo : [le placement sur les lignes (en anglais)](https://gridbyexample.com/video/series-line-based-placement/)
