---
title: HTML autofocus グローバル属性
short-title: autofocus
slug: Web/HTML/Reference/Global_attributes/autofocus
l10n:
  sourceCommit: 0754cd805a8e010d2e3a2a065f634a3bcf358252
---

**`autofocus`** [グローバル属性](/ja/docs/Web/HTML/Reference/Global_attributes)は論理属性で、ページ読み込み時、またはその要素が属する {{HTMLElement("dialog")}} が表示されたときに、その要素にフォーカスを当てるべきことを示す属性です。

```html
<input name="q" autofocus />
```

文書またはダイアログ内の複数の要素に autofocus 属性を設定することはできません。複数の要素に適用された場合、最初のものにフォーカスが当たります。

> [!NOTE]
> `autofocus` 属性は、フォームコントロールだけでなく、すべての要素に適用されます。例えば、これは [contenteditable](/ja/docs/Web/HTML/Reference/Global_attributes/contenteditable) の領域で使用されるかもしれません。

## アクセシビリティの考慮

フォームコントロールに自動的にフォーカスを合わせると、画面読み上げ技術を使用する視覚障碍者や認知障碍者を混乱させる可能性があります。`autofocus` が割り当てられている場合、スクリーンリーダーは事前に警告することなく、ユーザーをフォームコントロールに「テレポート」します。

`autofocus` 属性を使用する際には、アクセシビリティに十分配慮してください。コントロールに自動的にフォーカスが当たると、読み込む際にページのスクロールが発生する可能性があります。また、タッチ端末によっては、フォーカスが動的なキーボードを表示させることもあります。スクリーンリーダーはフォーカスを受けたフォームコントロールのラベルをアナウンスしますが、ラベルの前には何もアナウンスしないので、小さな機器にいる目の見えるユーザーは、前のコンテンツによって作成されたコンテキストを同様に見逃してしまうでしょう。

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}
