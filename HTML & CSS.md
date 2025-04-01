아래는 HTML과 CSS의 기본 문법을 설명한 `README.md` 파일 내용입니다.

```markdown
# HTML & CSS 기본 문법

## 1. HTML 기본 문법

HTML (HyperText Markup Language)은 웹 페이지의 구조를 정의하는 언어입니다. HTML은 다양한 **태그**를 사용하여 웹 페이지의 요소들을 구성합니다.

### 1.1 HTML 문서 구조

HTML 문서는 다음과 같은 기본 구조를 가집니다:

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

- `<!DOCTYPE html>`: HTML5 문서임을 선언합니다.
- `<html>`: HTML 문서의 시작을 나타내며, `lang="ko"`는 문서의 언어가 한국어임을 명시합니다.
- `<head>`: 문서의 메타데이터(제목, 문자 인코딩 등)를 포함하는 영역입니다.
- `<meta charset="UTF-8">`: 문자 인코딩을 UTF-8로 설정합니다.
- `<body>`: 웹 페이지의 실제 콘텐츠가 위치하는 부분입니다.

### 1.2 HTML 태그

HTML에서 자주 사용하는 태그들입니다:

- **헤더 태그**: `<h1>`, `<h2>`, ..., `<h6>` (문서 제목을 나타내는 태그)
  ```html
  <h1>메인 제목</h1>
  <h2>서브 제목</h2>
  ```

- **단락 태그**: `<p>` (단락을 나타내는 태그)
  ```html
  <p>여기는 문단입니다.</p>
  ```

- **링크 태그**: `<a href="URL">` (하이퍼링크를 생성하는 태그)
  ```html
  <a href="https://www.example.com">Example</a>
  ```

- **이미지 태그**: `<img src="이미지 경로" alt="대체 텍스트">` (이미지 삽입)
  ```html
  <img src="image.jpg" alt="설명 텍스트">
  ```

- **리스트 태그**: `<ul>`, `<ol>`, `<li>` (순서 없는 리스트, 순서 있는 리스트)
  ```html
  <ul>
    <li>아이템 1</li>
    <li>아이템 2</li>
  </ul>
  ```

### 1.3 HTML 속성

HTML 태그는 **속성(attribute)**을 가질 수 있습니다. 예를 들어:

- **`href` 속성**: `<a>` 태그에 링크 주소를 지정합니다.
- **`src` 속성**: `<img>` 태그에 이미지 파일 경로를 지정합니다.
- **`class` 속성**: CSS 스타일을 적용할 때 사용됩니다.

```html
<a href="https://www.example.com" class="link">링크</a>
<img src="image.jpg" alt="설명 텍스트" class="image">
```

## 2. CSS 기본 문법

CSS (Cascading Style Sheets)는 HTML 요소의 스타일을 지정하는 언어입니다. CSS는 **선택자**(selector)와 **속성**(property)을 사용하여 HTML 요소를 스타일링합니다.

### 2.1 CSS 문법

CSS 문법은 다음과 같은 형태입니다:

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

- `h1`: 스타일을 적용할 HTML 태그를 선택합니다.
- `color: red;`: 글자의 색을 빨간색으로 지정합니다.
- `font-size: 32px;`: 글자 크기를 32픽셀로 지정합니다.

### 2.2 CSS 선택자

CSS에서 다양한 선택자를 사용하여 특정 HTML 요소에 스타일을 적용할 수 있습니다.

- **태그 선택자**: 특정 HTML 태그를 선택합니다.
  ```css
  p {
    font-family: Arial, sans-serif;
  }
  ```

- **클래스 선택자**: `class` 속성 값을 기준으로 선택합니다. 클래스 이름 앞에 `.`을 붙입니다.
  ```css
  .button {
    background-color: blue;
    color: white;
  }
  ```

- **아이디 선택자**: `id` 속성 값을 기준으로 선택합니다. 아이디 이름 앞에 `#`을 붙입니다.
  ```css
  #header {
    font-size: 24px;
  }
  ```

- **자식 선택자**: 부모 요소 아래에 있는 자식 요소를 선택합니다.
  ```css
  div > p {
    color: green;
  }
  ```

### 2.3 CSS 속성

CSS에서 사용되는 주요 속성입니다:

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

- **margin**: 외부 여백을 지정합니다.
  ```css
  div {
    margin: 20px;
  }
  ```

- **padding**: 내부 여백을 지정합니다.
  ```css
  div {
    padding: 10px;
  }
  ```

- **border**: 테두리를 설정합니다.
  ```css
  div {
    border: 2px solid black;
  }
  ```

### 2.4 CSS 적용 방법

CSS는 여러 방식으로 HTML에 적용할 수 있습니다:

- **인라인 스타일**: HTML 태그의 `style` 속성을 사용하여 직접 스타일을 지정합니다.
  ```html
  <p style="color: red; font-size: 20px;">이것은 인라인 스타일입니다.</p>
  ```

- **내부 스타일 시트**: HTML 문서 내 `<style>` 태그를 사용하여 스타일을 지정합니다.
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

CSS에서는 모든 HTML 요소가 박스 형태로 렌더링됩니다. 이 박스는 네 가지 주요 부분으로 나뉩니다:

1. **컨텐츠 영역** (Content)
2. **패딩** (Padding) - 컨텐츠와 테두리 사이의 공간
3. **테두리** (Border) - 요소의 테두리
4. **마진** (Margin) - 요소와 다른 요소 사이의 공간

### 2.6 미디어 쿼리

미디어 쿼리는 화면 크기에 따라 스타일을 다르게 적용할 수 있는 방법입니다. 주로 반응형 디자인에 사용됩니다.

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

- 위 코드는 화면 너비가 600px 이하일 때 배경색을 `lightblue`로 변경합니다.

## 3. 결론

HTML과 CSS는 웹 페이지를 만들기 위한 기초적인 기술입니다. HTML을 사용해 구조를 정의하고, CSS로 스타일을 추가하여 웹 페이지를 더욱 아름답고, 사용자가 쉽게 사용할 수 있도록 만듭니다. 두 언어는 웹 개발에서 가장 중요한 도구로, 다양한 요소들을 꾸미고 상호작용할 수 있게 해줍니다.
```

이 파일을 `.md` 확장자로 저장하면 Markdown 형식으로 HTML과 CSS의 기본 문법을 잘 정리할 수 있습니다. Markdown을 지원하는 환경에서는 이 파일을 쉽게 볼 수 있습니다.
