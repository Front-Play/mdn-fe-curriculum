## 2-1-basic-html-syntax-and-structure.md

### 📝 나연

HTML 이란?
우리가 보는 웹페이지가 어떻게 구조화되어 있는지 브라우저로 하여금 알 수 있도록 하는 마크업 언어.

블록 레벨 요소 : 웹페이지 상에 블록(Block)을 만드는 요소

인라인 요소 : 항상 블록 레벨 요소 내에 포함되어 있음.

HTML 문서의 구조

```html
<!-- 문서의 형식을 나타냄 -->
<!DOCTYPE html>
<html>
  <!-- 검색 결과에 노출될 키워드 -->
  <head>
    <meta charset="utf-8" />
    <title>My test page</title>
  </head>
  <body>
    <p>This is my page</p>
  </body>
</html>
```

### 📝 은지

### 📝 정준

### 📝 주현

HTML의 구조

- 문서 상단에 doctype을 명시했다\_ 요즘은 !DOCTYPE html로 간단하게 명시한다
- head
  - 문자 인코딩, 제목 등의 정보`<meta charset="utf-8">`
  - 검색엔친 최적화를 위한 메타데이터 제공
  - 브라우저나 모바일에서 사용할 수 있는 아이콘을 등록
  - 스타일시트(css)나 js 파일에 연결
- body
  - 여는 태그(opening tag)
  - 닫는 태그(closing tag)
  - 내용(content)
  - 요소(element)
  - 빈 요소(단일 태그를 사용하는 경우\_ ex:img)
