## 2-1-basic-html-syntax-and-structure.md

### 📝 나연

### 📝 은지

### 📝 정준

1. **HTML이란?**

- 프로그래밍 언어가 아니라 브라우저가 웹 페이지의 구조를 알 수 있도록 하는 언어
- HTML은 element로 구성된다.

2. **Element**

- elements는 다시 여는 tags와 닫는 태그, 그리고 태그의 attribute & value, 태그 안의 content로 구성됩니다.
  - 즉, element의 시작과 끝은 tag로 표현됩니다.
  - element안에는 또 다른 element가 들어갈 수 있습니다.
- element는 block요소와 inline요소가 있습니다.
  - block: 새로운 줄을 만들어 냅니다.
  - inline: 새로운 줄을 만들어 내지 않습니다.

---

- 항상 닫는 tag가 있는 것은 아닙니다.
  - 예외) `<img />`, `<br />` 등

> `tags`는 대소문자를 구분하지 않습니다.

3. **attribute**

- element에 직접 표현되지는 않지만 추가적인 내용을 담습니다.
  - ex) `class`, `href`, `target` 등
- 속성의 value는 `''` 또는 `""`로 감싸줍니다.
  - 따옴표 안에서 따옴표 문자를 쓰고 싶다면 HTML entities를 사용한다.
  ```html
  <a href="http://www.example.com" title="Isn&#39;t this fun?"
    >A link to my example.</a
  >
  ```

4. **HTML 문서구조**

- `<!DOCTYPE html>`: 문서 형식
- `<html></html>`: 전체 페이지의 콘텐츠를 포함하는 기본 요소
- `<meta charset="utf-8">`: HTML 문서의 문자 인코딩 설정을 UTF-8로 지정
  - UTF-8에는 전세계에서 사용되는 언어에 대한 대부분의 문자가 포함
- `<title></title>`: 웹 페이지의 title을 지정
- `<body></body>`: 페이지에 표시되는 모든 콘텐츠를 포함하는 태그

5. **기타 사항**

- HTML에서 문자 `<`,`>`, `"`및 `&`는 특수 문자이다. 때문에 HTML 코드로 해석되지 않게 하기 위해서는 [ASCII코드](https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references)와 같은 방법을 사용한다.
- HTML 주석
  ```html
  <!-- <p>I am!</p> -->
  ```

---

6. **head 태그**

```html
<head>
  <meta charset="utf-8" />
  <title>My test page</title>
</head>
```

- `head`의 내용은 페이지에 표시되지 않는다.
- 구성

  - `<title>`: HTML 전체의 제목을 나타낸다. 이는 브라우저 탭에 표시된다.
    - 북마크 저장 시에도 이 title이 사용된다.
  - `<meta>`: 메타데이터를 나타내는 element로써, 데이터를 설명하는 데이터이다. - `name`: 어떤 메타데이터인지 나타낸다. - `content`: 실제 메타데이터의 내용이 담긴다.

    ```html
    <meta name="author" content="Chris Mills" />
    <meta
      name="description"
      content="The MDN Learning Area aims to provide
    complete beginners to the Web with all they need to know to get
    started with developing web sites and applications."
    />
    ```

    - 이러한 설명은 검색엔진에서 이 페이지가 노출될 확률을 높여준다. _**즉, SEO에 사용된다.**_
      - **예시보기:**
        ![ex1](https://github.com/Front-Play/mdn-fe-curriculum/assets/96231175/475d1d2a-5d7c-41e4-8925-daf01fa9f0e1)
        ![ex2](https://github.com/Front-Play/mdn-fe-curriculum/assets/96231175/f73d40f8-17a3-452f-a3d2-d8b09504d3aa)

    > ### 추가 참고
    >
    > - `<meta charset="utf-8" />`: 문서에서 허용하는 문자
    >
    >   - 집합(character set) encoding에 대해 간단히 표시한다.
    >   - `utf-8`은 전세계적으로 사용되는 집합으로 많은 언어의 문자들을 포함한다.  
    >     (즉, 어떠한 언어도 취급할 수 있도록 하는 것)

  - `OG(open-graph) tag`: meta(구 facebook)에서 보다 풍부한 메타데이터를 제공하기 위해 개발한 메타데이터 프로토콜

    - [참고 링크](https://ogp.me/)

    ```html
    <meta
      property="og:image"
      content="https://developer.mozilla.org/mdn-social-share.png"
    />
    <meta
      property="og:description"
      content="The Mozilla Developer Network (MDN) provides information about Open Web technologies including HTML, CSS, and APIs for both Web sites and HTML5 Apps. It also documents Mozilla products, like Firefox OS."
    />
    <meta property="og:title" content="Mozilla Developer Network" />
    ```

  - `favicon`추가하기

    - `<link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />`
    - 디바이스마다 해상도를 높이는 등 개별 적용도 가능하다.

  - CSS와 Javascript 적용

    - CSS: `<link rel="stylesheet" href="my-css-file.css" />`
    - JS: `<script src="my-js-file.js"></script>`

  - 문서 기본 언어 설정: `<html lang="en-US"></html>`

### 📝 주현
