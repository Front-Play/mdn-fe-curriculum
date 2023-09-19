## 2.6 Media

### 📝 나연

### 📝 은지

### 📝 정준

### 1. 이미지

- 태그 사용법:

  1. 상대 경로 지정
  2. 절대 경로 지정

  ```html
  <!-- 1 -->
  <img src="images/dinosaur.jpg" alt="Dinosaur" />
  <!-- 2 -->
  <img src="https://www.example.com/images/dinosaur.jpg" alt="Dinosaur" />
  ```

  - `alt`속성: 이미지의 설명을 나타냅니다. 이는 이미지가 느리게 로딩되거나 로딩되지 않았을 떄 이미지에 대한 정보를 나타낼 수 있고, 장애가 있는 분들에게 정보를 제공할 수 있습니다.
  - `alt`안에는 무엇을 써야하는가? 용도에 따라 다르다.
    - **Decoration**: 꾸미는 요소는 _CSS_ 의 `background-image`를 사용하는 것이 좋지만 부득이하게 HTML을 쓸 경우에는 빈 `""`값으로 둔다.
      - 오히려 스크린 리더가 읽는데 낭비하는 시간을 줄일 수 있다.
    - **Content**: 이미지가 중요한 정보라면 설명을 적어준다.
    - **Link**: `<a>`태그로 이미지를 감싸 링크를 연결하고자 한다면 `<a>`태그 뿐 아니라 `alt`값 안에 넣을 수도 있다.
    - **Text**: 텍스트로 된 이미지를 넣어선 안된다. 다만 마찬가지로 부득이하게 사용할 경우에는 해당 텍스트 정보를 넣어준다.
  - `title`: 이미지에 hover했을 때 나타낼 텍스트 지정

  > ### 이미지 요소의 너비와 높이는 지정해주는 것이 좋다.
  >
  > - 이유: 페이지가 렌더링될 떄 HTML요소와 이미지는 별개로 로딩되는데, 이떄 보통은 이미지가 데이터 크기가 더 크기 때문에 더 늦게 로딩된다.
  >   - 그렇기 때문에 로딩되기 전까지 이미지가 페이지에서 차지하고 있는 영역을 공백으로라도 잡아두어 사용자에게 갑자기 이미지가 추가되는 어색함을 주지 않기 위해 크기를 지정해주는 것이 좋다.

  - `figure` & `figcaption`: 이미지의 주석을 표기하는 태그

### 2. Video

- `video`태그와 사용법 보기

```html
<video
  controls
  width="400"
  height="400"
  autoplay
  loop
  muted
  preload="auto"
  poster="poster.png"
>
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>
    Your browser doesn't support this video. Here is a
    <a href="rabbit320.mp4">link to the video</a> instead.
  </p>
</video>
```

- `audio`태그와 사용법 보기

```html
<audio controls>
  <source src="viper.mp3" type="audio/mp3" />
  <source src="viper.ogg" type="audio/ogg" />
  <p>
    Your browser doesn't support this audio file. Here is a
    <a href="viper.mp3">link to the audio</a> instead.
  </p>
</audio>
```

### 3. Embedding

- **Embedding**을 통해 파일이나 다른 웹 페이지를 담아서 표현할 수 있다.

#### 방법 보기:

1. `<iframe>`: 현재 문서에 다른 문서(웹 페이지)를 표기

- ```html
  <head>
    <style>
      iframe {
        border: none;
      }
    </style>
  </head>
  <body>
    <iframe
      src="https://developer.mozilla.org/ko/docs/Glossary"
      width="100%"
      height="500"
      allowfullscreen
      sandbox
    >
      <p>
        <a href="/ko/docs/Glossary">
          iframes을 지원하지 않는 브라우저용 링크
        </a>
      </p>
    </iframe>
  </body>
  ```

2. `<embed>`와 `<object>`: iframe과는 다르게 외부 pdf자료 등을 표현하기 위한 태그이다.

- ```html
  <object data="mypdf.pdf" type="application/pdf" width="800" height="1200">
    <p>
      You don't have a PDF plugin, but you can
      <a href="mypdf.pdf">download the PDF file. </a>
    </p>
  </object>
  ```

### 4. 이미지와 관련된 추가 정보

1. `<svg>`태그: 웹에 벡터 그래픽을 추가할 수 있다.

- 장점:
  - HTTP 요청이 절약되므로 로딩 시간을 조금 줄일 수 있다.
  - CSS로 스타일을 지정
- 단점:
  - SVG를 한 곳에서만 사용하는 경우에만 적합하다.
  - 추가 SVG 코드는 HTML 파일의 크기를 증가시킨다.
  - 브라우저는 일반 이미지 자산을 캐시하는 것처럼 인라인 SVG를 캐시할 수 없다.
    - 즉, 다음 로딩 시에도 똑같이 시간이 걸린다.

2. 반응형 이미지 만들기

- ```html
  <img
    srcset="elva-fairy-480w.jpg 480w, elva-fairy-800w.jpg 800w"
    sizes="(max-width: 600px) 480px,
           800px"
    src="elva-fairy-800w.jpg"
    alt="요정 옷을 입은 엘바"
  />
  ```

  - `srcset`: 파일별로 값을 지정한다. (이름 + 공백 + 고유 크기 지정)
    - `px`이 아니라 `w`를 사용한다는 점에 유의한다.
  - `sizes`: 화면 사이즈에 맞춰 이미지 크기를 변경한다.

3. `<picture>`: video나 audio처럼 source를 제공한다.

- ```html
  <picture>
    <source media="(max-width: 799px)" srcset="elva-480w-close-portrait.jpg" />
    <source media="(min-width: 800px)" srcset="elva-800w.jpg" />
    <img src="elva-800w.jpg" alt="딸 엘바를 안고 서 있는 크리스" />
  </picture>
  ```

### 📝 주현
