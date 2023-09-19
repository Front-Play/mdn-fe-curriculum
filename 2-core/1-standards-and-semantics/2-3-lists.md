## 2.3 Lists

### 📝 나연

1. 순서가 없는 리스트

```html
<ul>
  <li>milk</li>
  <li>eggs</li>
  <li>bread</li>
  <li>hummus</li>
</ul>
```

2. 순서가 있는 리스트

```html
<ol>
  <li>Drive to the end of the road</li>
  <li>Turn right</li>
  <li>Go straight across the first two roundabouts</li>
  <li>Turn left at the third roundabout</li>
  <li>The school is on your right, 300 meters up the road</li>
</ol>
```

3. 설명

```html
<!-- 설명 목록 요소 -->
<dl>
  <!-- 설명 용어 요소  -->
  <dt>
    <!--설명 세부 요소  -->
  </dt>

  <dd>
    <!-- 전체 구조 -->
    <dl>
      <dt>Denim (semigloss finish)</dt>
      <dd>Ceiling</dd>

      <dt>Denim (eggshell finish)</dt>
      <dt>Evening Sky (eggshell finish)</dt>
      <dd>Layered on the walls</dd>
    </dl>
  </dd>
</dl>
```

4. 인용

```html
<!-- 블록 수준 콘텐츠 섹션(단락, 여러 단락, 목록 등)이 다른 곳에서 인용된 경우 -->
<blockquote>
  <!-- 인라인 인용 -->
  <q></q>
</blockquote>
```

### 📝 은지
#### HTML text fundamentals
HTML의 주요 작업 중 하나는 브라우저가 텍스트를 올바르게 표시 할 수 있도록 텍스트 구조와 의미를 제공하는 것(시멘틱)

### 구조가 필요한 이유(<p> 등)

- 브라우저가 어떤게 heading이고 어떤게 문단인지 알 수 없다
- 사용자가 주로 heading만 읽는 경우도 있는데 파악하기 어렵다
- 검색 엔진들은 우리 페이지 내의 heading을 페이지 검색 순위에 영향을 주는 중요한 키워드로 고려해 indexing을 한다. heading이 없으면 SEO가 형편없어짐
- 시각장애인들을 웹 페이지를 읽지못하기 때문에 스크린 리더로 주로 읽는다. 그 때 heading을 읽어줌으로써 무슨 콘텐츠인지 파악할 수 있다.

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
