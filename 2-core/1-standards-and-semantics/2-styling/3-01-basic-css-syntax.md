## 3.1 Basic CSS syntax

### 📝 나연

#### CSS 란?

사용자에게 문서를 표시하는 방법을 지정하는 언어!

항상 브라우저 지원 상태를 확인하는 자세가 필요하다!

```html
<!-- styles.css 파일을 index.html 에 링크 -->
<link rel="stylesheet" href="styles.css" />
```

#### 문서에서의 위치에 따라 스타일 지정하기

```css
/* li 요소 안에 중첩된 em 만 선택 */
li em {
  color: rebeccapurple;
}

/* 동일한 계층 구조 수준에서 제목 바로 다음에 오는 단락의 스타일 지정 */
h1 + p {
  font-size: 200%;
}
```

#### 상태에 따른 스타일링

```css
a:link {
  color: pink;
}

a:visited {
  color: green;
}
```

### 📝 은지

### 📝 정준

### 📝 주현
