## 2.3 Lists

### 📝 나연

### 📝 은지

### 📝 정준

### HTML text fundamentals - lists

> `HTML text fundamentals`: HTML의 주요 역할 중 하나로써 브라우저가 텍스트를 잘 표현할 수 있도록 구조와 의미를 제공하는 것.

**1. 제목과 단락**

제목과 단락을 구분하여 컨텐츠를 구조화합니다.

- 제목: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
- 단락: `<p>`

**2. 구조화는 왜 필요한가?**

1. 구조화를 통해 사용자에게 가독성 높은 컨텐츠를 제공합니다.
2. 검색 엔진에서 제목(heading)을 검색 순위에 영향을 주는 중요한 키워드로 익식하여 indexing합니다.  
   -> **`검색 엔진 최적화`**
3. 시각 장애인들에게 필요한 정보를 빠르게 전달할 수 있습니다.
4. CSS, Javascript를 효과적으로 적용할 수 있습니다.

**3. Semantic Tag**

- `tag`자체만으로 의미를 파악할 수 있도록 한 것을 말합니다.
  - 때문에 태그명만으로 해당 컨텐츠가 담고 있는 내용을 유추하고 의미를 확인할 수 있습니다.

---

### Advanced text formatting

#### 1. Lists

1. Unordered: `<ul>`
2. Ordered: `<ol>`
3. Nesting lists: **list내의 list**

#### 2. Description lists

- 설명을 포함하는 리스트

```html
<dl>
  <dt>제목</dt>
  <dd>설명</dd>
</dl>
```

#### 3. Quotations

1. `<blackquote>`
2. `<q>`

- 인용구를 표시할 때 사용
- `cite` 속성: 출처 표시
  - 그러나 브라우저나 스크린 리더가 이를 활용할 방안은 많지 않기 때문에 페이지에 표시하기 위해선 추가적인 작업 필요

```html
<p>다음은 블록 인용구입니다.</p>
<blockquote
  cite="https://developer.mozilla.org/ko/docs/Web/HTML/Element/blockquote"
>
  <p>
    <strong>HTML <code>&lt;blockquote&gt;</code> 요소</strong> (또는
    <em>HTML 인용 블록 요소</em>)는 안쪽의 텍스트가 긴 인용문임을 나타냅니다.
  </p>
</blockquote>

<p>
  인용구 요소 — <code>&lt;q&gt;</code> — 는
  <q cite="https://developer.mozilla.org/ko/docs/Web/HTML/Element/q">
    단락 나누기가 필요 없는 짧은 인용구를 위한 것입니다.
  </q>
</p>
```

#### 4. Abbreviations

- `<addr>`: 약어를 표기할 때 사용
  - 예시:
  ```html
  <abbr title="Reverend">Rev.</abbr>
  ```

#### 5. Contact detail

- 연락처를 태그로 표시: `<address>`

#### 6. Superscript and subscript

- `<sup>` & `<sub>`: 각각 위첨자와 아래첨자 표기

#### 7. Computer code

- `<code>`: 컴퓨터 코드를 표시
- `<pre>`: 공백(일반적으로 코드 블록)을 유지하기 위해 사용 택스트 내에서 들여 쓰기 또는 초과 공백을 사용하면 브라우저가 이를 무시하고 렌더링 된 페이지에 공백을 표시하지 않습니다.
  - `<pre></pre>` 태그로 텍스트를 감싸면 공백이 텍스트 편집기에서 보는 것과 동일하게 렌더링
- `<kbd>`: 컴퓨터에 입력 된 키보드 (및 기타 유형) 입력을 표시
- `<samp>`: 컴퓨터 프로그램의 출력을 표시

#### 8. Time & Date

- `<time>`: 시간과 날짜에 대해서 표기합니다
  - 예시:
  ```html
  <time datetime="2016-01-20T19:30+01:00">
    7.30pm, 20 January 2016 is 8.30pm in France
  </time>
  ```

> 출처: [MDN](https://developer.mozilla.org/ko/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting#%EC%BB%B4%ED%93%A8%ED%84%B0_%EC%BD%94%EB%93%9C%EB%A5%BC_%EB%82%98%ED%83%80%EB%82%B4%EA%B8%B0)

### 📝 주현
