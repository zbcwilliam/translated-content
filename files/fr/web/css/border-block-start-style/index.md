---
title: border-block-start-style
slug: Web/CSS/border-block-start-style
---

{{CSSRef}}{{SeeCompatTable}}

La propriété **`border-block-start-style`** définit le style de la bordure utilisé pour le côté du début de l'élément dans l'axe orthogonal au sens de lecture. Cette propriété logique correspondra à une propriété physique selon le mode d'écriture, la directionnalité et l'orientation du texte. Autrement dit, elle correspond à {{cssxref("border-top-style")}}, {{cssxref("border-right-style")}}, {{cssxref("border-bottom-style")}} ou à {{cssxref("border-left-style")}} selon les valeurs de {{cssxref("writing-mode")}}, {{cssxref("direction")}} et {{cssxref("text-orientation")}}.

{{InteractiveExample("CSS Demo: border-block-start-style")}}

```css interactive-example-choice
border-block-start-style: dotted;
writing-mode: horizontal-tb;
```

```css interactive-example-choice
border-block-start-style: dotted;
writing-mode: vertical-rl;
```

```css interactive-example-choice
border-block-start-style: groove;
writing-mode: horizontal-tb;
```

```css interactive-example-choice
border-block-start-style: dashed;
writing-mode: vertical-lr;
```

```html interactive-example
<section class="default-example" id="default-example">
  <div class="transition-all" id="example-element">
    This is a box with a border around it.
  </div>
</section>
```

```css interactive-example
#example-element {
  background-color: #eee;
  color: #000;
  border: 0.75em solid;
  padding: 0.75em;
  width: 80%;
  height: 100px;
  unicode-bidi: bidi-override;
}
```

Les autres propriétés logiques permettant de définir le style de la bordure sont les suivantes :

- {{cssxref("border-inline-start-style")}}
- {{cssxref("border-inline-end-style")}}
- {{cssxref("border-block-end-style")}}.

## Syntaxe

```css
/* border-block-start-style: style */
border-block-start-style: dashed;
border-block-start-style: dotted;
border-block-start-style: groove;
```

### Valeurs

- `<'border-style'>`
  - : Le style utilisé pour la ligne de la bordure, voir {{cssxref("border-style")}}.

## Définition formelle

{{CSSInfo}}

## Syntaxe formelle

{{CSSSyntax}}

## Exemples

### CSS

```css
div {
  background-color: yellow;
  width: 120px;
  height: 120px;
}

.exemple {
  writing-mode: vertical-lr;
  border: 5px solid blue;
  border-block-start-style: dashed;
}
```

### HTML

```html
<div>
  <p class="exemple">Texte d'exemple</p>
</div>
```

### Résultat

{{EmbedLiveSample("Exemples", 140, 140)}}

## Spécifications

{{Specifications}}

## Compatibilité des navigateurs

{{Compat}}

## Voir aussi

- Les propriétés physiques correspondantes :
  - {{cssxref("border-top-style")}},
  - {{cssxref("border-right-style")}},
  - {{cssxref("border-bottom-style")}},
  - {{cssxref("border-left-style")}}

- {{cssxref("writing-mode")}}, {{cssxref("direction")}}, {{cssxref("text-orientation")}}
