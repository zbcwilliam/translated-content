---
title: 레이아웃 이해의 핵심 사항
slug: Learn_web_development/Core/CSS_layout/Fundamental_Layout_Comprehension
original_slug: Learn/CSS/CSS_layout/Fundamental_Layout_Comprehension
l10n:
  sourceCommit: 751d58669499de0c6ea0d5b356e0e1448418c5d3
---

{{LearnSidebar}}
{{PreviousMenu("Learn/CSS/CSS_layout/Supporting_Older_Browsers", "Learn/CSS/CSS_layout")}}

이 과정을 학습했다면 현재 CSS 레이아웃을 만들고 이전 CSS로 작업하기 위해 알아야 할 기본 사항을 이미 다루었을 것입니다. 이 과제는 다양한 기법을 사용하여 간단한 웹 페이지 레이아웃을 개발하는 방식으로 지식을 테스트할 것입니다.

<table>
  <tbody>
    <tr>
      <th scope="row">필요한 사전 지식:</th>
      <td>
        이 평가를 시도하기 전에 이 과정의 모든 문서를 이미 완료해야 합니다.
      </td>
    </tr>
    <tr>
      <th scope="row">목표:</th>
      <td>
        플렉스박스, 그리드, 플로팅, 그리고 포지셔닝을 사용하는 CSS 레이아웃 메서드에 대한 이해도를 테스트합니다.
      </td>
    </tr>
  </tbody>
</table>

## 시작점

[여기](https://github.com/mdn/learning-area/tree/main/css/css-layout/fundamental-layout-comprehension)에서 HTML, CSS 및 6개의 이미지 세트를 다운로드할 수 있습니다.

HTML 문서와 스타일시트를 컴퓨터의 디렉터리에 저장하고, 이미지를 `images`라는 폴더에 추가합니다. 브라우저에서 `index.html` 파일을 열면 기본 스타일은 있지만 레이아웃이 없는 페이지가 표시되며, 아래 이미지와 비슷하게 보일 것입니다.

![레이아웃 작업의 시작점입니다. 요소가 깔끔하게 배치되지 않았습니다. 왼쪽에 5개의 링크가 있는 검은색 네비게이션 바 위에 웹 사이트 제목이 있고, 그 뒤에 블로그 글 제목과 글 내용이 있습니다. 블로그 제목과 블로그 내용 사이에는 왼쪽 끝에 맞춰진 사진이 있습니다.](layout-task-start.png)

이 시작점에는 정상적인 흐름에서 브라우저에 표시되는 레이아웃의 모든 콘텐츠가 있습니다.

또는 [Glitch](https://glitch.com/)와 같은 사이트를 사용하여 HTML과 CSS를 붙여넣어 평가를 수행할 수 있습니다. 온라인 편집기를 사용하는 경우 이미지를 업로드하고 새 이미지 위치를 가리키도록 `src` 특성의 값을 바꿔야 합니다. 사용 중인 온라인 편집기에 별도의 CSS 패널이 없는 경우 문서 head의 `<style>` 요소에 자유롭게 넣어도 됩니다.

> [!NOTE]
> 문제가 발생하면, 이 페이지 하단의 [평가 또는 추가 도움말](#assessment_or_further_help) 섹션을 참조하여 도움을 요청하세요.

## 프로젝트 요약

가공되지 않은 HTML, 기본 CSS 및 이미지가 제공되었으므로 이제 디자인을 위한 레이아웃을 만들어야 합니다.

### 작업

이제 레이아웃을 구현해야 합니다. 달성해야 할 작업은 다음과 같습니다.

1. 내비게이션 항목을 항목 사이에 동일한 간격으로 일렬로 표시합니다.
2. 내비게이션 바가 콘텐츠와 함께 스크롤되다가 콘텐츠에 도달하면 뷰포트 상단에 고정되도록 합니다.
3. 문서 내부의 이미지에 텍스트가 둘러싸여 있어야 합니다.
4. {{htmlelement("article")}}과 {{htmlelement("aside")}} 요소는 두 개의 열 레이아웃으로 표시되어야 합니다. 열은 브라우저 창이 작아지면 열이 좁아지도록 유연한 크기여야 합니다.
5. 사진은 이미지 사이에 1픽셀 간격이 있는 두 열 그리드로 표시되어야 합니다.

## 힌트 및 팁

이 레이아웃을 구현하기 위해 HTML을 편집할 필요는 없으며 사용해야 하는 기술은 다음과 같습니다:

- 플렉스박스
- 그리드
- Floating
- Positioning

이러한 작업 중 일부를 달성할 수 있는 몇 가지 방법이 있으며, 옳고 그름이 따로 정해져 있지 않은 경우가 많습니다. 몇 가지 다른 접근 방식을 시도해 보고 어떤 방법이 가장 효과적인지 알아보세요. 실험하면서 메모해 두세요.

## 예제

다음 스크린샷은 완성된 디자인 레이아웃의 예제를 보여 줍니다.

![웹 사이트 레이아웃 작업을 마쳤습니다. 요소가 깔끔하게 배치되었습니다. 동일한 간격의 링크 5개가 포함된 검은색 네비게이션 바 위에 웹 사이트 제목이 있습니다. 네비게이션 바 아래에는 두 개의 섹션이 있습니다. 왼쪽에는 블로그 글이 있습니다. 블로그 글 제목 다음에 글 내용이 표시됩니다. 블로그 내용은 왼쪽에 있는 사진을 감싸고 있습니다. 오른쪽에는 두 장의 이미지가 너비가 넓은 그리드에 배치된 이미지 그룹에 대한 'Photography' 제목이 있습니다.](layout-task-complete.png)

## 평가 또는 추가 도움말

작업 평가를 받고 싶거나 막혀서 도움을 요청하고 싶은 경우, 다음을 참고하시면 됩니다.

1. [CodePen](https://codepen.io/), [jsFiddle](https://jsfiddle.net/), 또는 [Glitch](https://glitch.com/)와 같은 온라인 공유 가능 편집기에 작업을 넣습니다.
2. [MDN Discourse forum Learning category](https://discourse.mozilla.org/c/mdn/learn/250)에서 평가 또는 도움, 혹은 평가와 도움 모두를 요청하는 게시물을 작성합니다. 게시물에는 다음이 포함되어야 합니다.
   - "레이아웃 이해의 핵심 사항에 대한 평가가 필요합니다"와 같은 설명이 포함된 제목이 포함되어야 합니다.
   - 이미 시도해 본 내용과 저희가 해 주었으면 하는 것에 대한 세부 사항이 포함되어야 합니다. 예를 들어, 막혀서 도움이 필요하거나 평가를 원하는 경우를 알려 주면 됩니다.
   - (위 1단계에서 언급한 대로) 온라인 공유 가능한 편집기에서 평가받거나 도움이 필요한 예제에 대한 링크를 준비합니다. 코드를 볼 수 없다면 코딩 문제가 있는 사람을 도와 주기가 매우 어렵기 때문에 이 방법을 사용하는 것이 좋습니다.
   - 실제 작업 또는 평가 페이지로 연결되는 링크를 통해 도움을 원하는 문제를 찾을 수 있습니다.

{{PreviousMenu("Learn/CSS/CSS_layout/Supporting_Older_Browsers", "Learn/CSS/CSS_layout")}}
