## 2.4 Advanced text techniques

### 📝 나연

1. 중요

특정 단어에 강세를 두고 발음하기 위해서는 `em` 태그를 사용해야함. 실제로 화면판독기에 인식되면 다른 톤의 목소리로 표현해준다고 한다!

2. 강조

`<strong>` 사용
`<span>` 요소에 약간의 CSS
`<b>` 사용

### 📝 은지

### 📝 정준

### HTML text fundamentals - Emphasis and importance

> `HTML text fundamentals`: HTML의 주요 역할 중 하나로써 브라우저가 텍스트를 잘 표현할 수 있도록 구조와 의미를 제공하는 것.

### 강세와 강조

**1. Emphasis**

  - HTML에서 단어에 강세를 넣기 위해선 이텔릭체를 사용한다.
  - 이때 사용하는 tag가 `<em>`태그이다.
    ```html
    <p>I am <em>glad</em> you weren't <em>late</em>.</p>
    ```

**2. Strong importance**

  - HTML에서 단어를 강조하기 위해선 두꺼운 글씨체로 표현한다.
  - 이때 사용하는 tag가 `<strong>`태그이다.
    ```html
    <p>This liquid is <strong>highly toxic</strong>.</p>
    <p>I am counting on you. <strong>Do not</strong> be late!</p>
    ```

### 기타 참고

**presentational elements**

  - CSS가 제대로 발전되지 않고, 잘 적용되지 않던 시절 사용하던 **presentational elements**라고 불리는 tag들이 있다.
    - `<b>`, `<i>`, `<u>`
    - 이들은 각각 bold, italic, underline을 뜻한다.
  - 이 같은 태그는 사용이 지양되어야 한다.
  ---
  **Why?**
  1. UX에 혼란을 야기할 수 있다.  
    - 예를 들면, 웹페이지에서 사용자는 밑줄이 쳐진 text를 하이퍼링크로 인식할 수 있다.
  2. SEO 등에 적합하지 않다.  
    - 의미를 담고 있는 semantic 태그와 달리 위 태그는 의미를 담고 있지 않아 SEO에 적합하지 않다.
  ---
  즉, 위 같은 이유로 현재 의미를 정립해 놓은 semantic의 사용을 지향해야 한다.  
  HTML5에서 위 세개의 태그는 아래와 같이 재정립되었으므로, 다른 적합한 tag가 없고, 부득이한 경우 아래와 같은 의미를 가지고 사용한다.

  - `<i>`: 요소는 과거로부터 줄곧 기울임꼴로 전달되는 의미를 전달하기 위해 사용된다. 외래어, 분류학 명칭, 전문 용어, 생각...
  - `<b>`: 요소는 과거로부터 줄곧 굵은 글씨로 전달되는 의미를 전달할 때 사용한다. 주요 단어, 제품 이름, 주요 문장...
  - `<u>`: 요소는 과거로부터 줄곧 밑줄을 치는 것으로 전달되는 의미를 전달할 떄 사용한다. 적절한 이름, 잘못된 철자...

### 📝 주현
