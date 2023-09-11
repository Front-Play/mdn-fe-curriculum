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
    <a href='http://www.example.com' title='Isn&#39;t this fun?'>A link to my example.</a>
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

### 📝 주현
