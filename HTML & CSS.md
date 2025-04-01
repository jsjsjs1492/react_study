
# HTML & CSS 기본 문법

HTML과 CSS는 웹 페이지를 만드는 데 필요한 기초적인 언어입니다. HTML은 웹 페이지의 구조를 정의하고, CSS는 그 구조에 스타일을 추가하는 역할을 합니다.

## 1. HTML 기본 문법

HTML (HyperText Markup Language)은 웹 페이지의 구조를 정의하는 언어입니다. HTML 문서는 다양한 **태그**를 사용하여 웹 페이지의 요소들을 정의합니다.

### 1.1 HTML 문서 구조

HTML 문서는 기본적으로 아래와 같은 구조를 가집니다:

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>문서 제목</title>
</head>
<body>
  <h1>안녕하세요, HTML!</h1>
  <p>HTML은 웹 페이지를 구성하는 언어입니다.</p>
</body>
</html>
```

#### HTML 문서의 기본 구성 요소:

- **`<!DOCTYPE html>`**: HTML5 문서임을 선언하는 선언문입니다. 이 선언은 문서의 첫 번째 줄에 위치해야 합니다.
- **`<html>`**: HTML 문서의 루트(root) 요소입니다. 모든 HTML 콘텐츠는 `<html>` 태그 안에 포함됩니다. `lang="ko"`는 이 문서의 언어가 한국어임을 나타냅니다.
- **`<head>`**: 문서의 메타데이터를 포함하는 영역입니다. 여기에는 문자 인코딩, 스타일 시트 링크, 페이지 제목 등이 들어갑니다.
- **`<meta charset="UTF-8">`**: 문서의 문자 인코딩을 `UTF-8`로 설정합니다. 이는 다국어 문자 지원을 위해 중요합니다.
- **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**: 모바일 화면에서 적절한 화면 크기와 비율을 설정합니다.
- **`<title>`**: 브라우저 탭에 표시될 페이지의 제목을 설정합니다.
- **`<body>`**: 실제 웹 페이지에 표시되는 콘텐츠를 포함하는 부분입니다.

### 1.2 HTML 태그

HTML에서는 여러 태그를 사용하여 문서의 다양한 요소를 정의합니다. 주요 태그들을 소개합니다.

- **헤더 태그** (`<h1>`, `<h2>`, ..., `<h6>`)  
  제목을 정의할 때 사용합니다. `<h1>`은 가장 중요한 제목, `<h2>`는 그다음 제목 등으로 크기가 줄어듭니다.
  
  ```html
  <h1>메인 제목</h1>
  <h2>서브 제목</h2>
  ```

- **단락 태그** (`<p>`)  
  단락을 정의합니다. 텍스트를 묶어 표현할 때 사용됩니다.
  
  ```html
  <p>이것은 단락입니다. 여러 문장이 포함될 수 있습니다.</p>
  ```

- **링크 태그** (`<a href="URL">`)  
  하이퍼링크를 만들 때 사용합니다. `href` 속성에 링크할 URL을 지정합니다.
  
  ```html
  <a href="https://www.example.com">Example 웹사이트</a>
  ```

- **이미지 태그** (`<img src="이미지 경로" alt="대체 텍스트">`)  
  이미지를 페이지에 삽입합니다. `src` 속성에 이미지 파일 경로를 지정하고, `alt` 속성은 이미지가 로드되지 않았을 때 대신 표시할 텍스트입니다.
  
  ```html
  <img src="image.jpg" alt="설명 텍스트">
  ```

- **리스트 태그** (`<ul>`, `<ol>`, `<li>`)  
  순서가 없는 리스트(`<ul>`)와 순서가 있는 리스트(`<ol>`)를 만들 수 있습니다. 각각의 항목은 `<li>` 태그로 정의됩니다.
  
  ```html
  <ul>
    <li>아이템 1</li>
    <li>아이템 2</li>
  </ul>
  ```

### 1.3 HTML 속성

HTML 태그는 속성을 추가하여 더 많은 기능을 제공할 수 있습니다.

- **`href`**: `<a>` 태그에서 링크를 지정하는 속성입니다.
- **`src`**: `<img>` 태그에서 이미지 파일 경로를 지정하는 속성입니다.
- **`class`**: CSS에서 스타일을 적용할 때 사용됩니다. 여러 HTML 요소에 공통 스타일을 적용할 때 유용합니다.
- **`id`**: HTML 문서에서 각 요소를 고유하게 식별할 때 사용됩니다. CSS나 JavaScript에서 특정 요소를 쉽게 선택할 수 있습니다.

```html
<a href="https://www.example.com" class="link">Example 링크</a>
<img src="image.jpg" alt="설명 텍스트" class="image">
```

## 2. CSS 기본 문법

CSS (Cascading Style Sheets)는 HTML 요소의 스타일을 지정하는 언어입니다. CSS는 HTML 문서의 외형을 꾸미는 데 사용됩니다. CSS 문법은 **선택자**(selector)와 **속성**(property)으로 구성됩니다.

### 2.1 CSS 문법

CSS 문법은 다음과 같은 형태로 작성됩니다:

```css
선택자 {
  속성: 값;
}
```

예시:

```css
h1 {
  color: red;
  font-size: 32px;
}
```

- **선택자**: 스타일을 적용할 HTML 요소를 지정합니다.
- **속성**: 요소의 스타일을 지정하는 속성입니다.
- **값**: 해당 속성의 값을 설정합니다.

### 2.2 CSS 선택자

CSS에서 선택자는 스타일을 적용할 HTML 요소를 지정하는 방법입니다. 주요 선택자는 다음과 같습니다.

- **태그 선택자**: 특정 HTML 태그를 선택하여 스타일을 적용합니다.
  
  ```css
  p {
    font-family: Arial, sans-serif;
  }
  ```

- **클래스 선택자**: `class` 속성을 기준으로 스타일을 적용합니다. 클래스 이름 앞에 `.`을 붙입니다.
  
  ```css
  .button {
    background-color: blue;
    color: white;
  }
  ```

- **아이디 선택자**: `id` 속성을 기준으로 스타일을 적용합니다. 아이디 이름 앞에 `#`을 붙입니다.
  
  ```css
  #header {
    font-size: 24px;
  }
  ```

- **자식 선택자**: 특정 부모 요소의 자식 요소만 선택하여 스타일을 적용합니다.
  
  ```css
  div > p {
    color: green;
  }
  ```

### 2.3 CSS 속성

CSS에서 사용되는 주요 속성들입니다:

- **color**: 글자 색을 지정합니다.
  
  ```css
  p {
    color: blue;
  }
  ```

- **background-color**: 배경색을 지정합니다.
  
  ```css
  body {
    background-color: lightgray;
  }
  ```

- **font-size**: 글자 크기를 지정합니다.
  
  ```css
  h1 {
    font-size: 36px;
  }
  ```

- **margin**: 요소의 바깥쪽 여백을 설정합니다.
  
  ```css
  div {
    margin: 20px;
  }
  ```

- **padding**: 요소의 안쪽 여백을 설정합니다.
  
  ```css
  div {
    padding: 10px;
  }
  ```

- **border**: 요소의 테두리를 설정합니다.
  
  ```css
  div {
    border: 2px solid black;
  }
  ```

### 2.4 CSS 적용 방법

CSS는 HTML 문서에 여러 가지 방법으로 적용할 수 있습니다.

- **인라인 스타일**: HTML 태그 내에 `style` 속성을 사용하여 스타일을 지정합니다.
  
  ```html
  <p style="color: red; font-size: 20px;">이것은 인라인 스타일입니다.</p>
  ```

- **내부 스타일 시트**: HTML 문서의 `<head>` 섹션에 `<style>` 태그를 사용하여 스타일을 작성합니다.
  
  ```html
  <style>
    h1 {
      color: blue;
    }
  </style>
  ```

- **외부 스타일 시트**: 별도의 `.css` 파일을 만들어 링크하여 스타일을 적용합니다.
  
  ```html
  <link rel="stylesheet" href="styles.css">
  ```

### 2.5 CSS 박스 모델

CSS에서 모든 HTML 요소는 박스 형태로 렌더링됩니다. 이 박스는 네 가지 주요 부분으로 나눠집니다:

1. **컨텐츠 영역** (Content)
2. **패딩** (Padding) - 컨텐츠와 테두리 사이의 공간
3. **테두리** (Border) - 요소의 테두리
4. **마진** (Margin) - 요소와 다른 요소 사이의 공간

### 2.6 미디어 쿼리

미디어 쿼리는 화면 크기나 장치의 특성에 따라 스타일을 다르게 적용하는 방법입니다. 반응형 디자인에 사용됩니다.

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

- 위 코드는 화면 너비가 600px 이하일 때 배경색을 `lightblue`로 변경합니다.

## 3. 결론

HTML과 CSS는 웹 페이지를 만드는 데 필수적인 언어입니다. HTML은 웹 페이지의 구조를 정의하고, CSS는 그 구조를 꾸미는 역할을 합니다. HTML과 CSS를 잘 활용하면 사용자에게 보기 좋은, 기능적인 웹 페이지를 만들 수 있습니다.
```
