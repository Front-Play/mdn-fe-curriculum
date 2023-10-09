## 2.6 Media

### 📝 나연

#### 이미지

```html
<img src="dinosaur.jpg" alt="Dinosaur" width="400" height="341" />
<!-- alt : 이미지에 대한 텍스트 설명 
 인터넷이 느려서 이미지를 보거나 표시할 수 없는 경우 -->

<!-- 미리 width / height 값을 설정하자. -->
```

#### 비디오 / 오디오

비디오, 오디오에서도 마찬가지로 width, height 미리 설정
컨트롤 태그사용하면 사용자가 컨트롤할 수 있음.

```html
<video src="rabbit320.webm" controls>
  <p>
    Your browser doesn't support HTML video. Here is a
    <a href="rabbit320.webm">link to the video</a> instead.
  </p>
</video>

<audio controls>
  <source src="viper.mp3" type="audio/mp3" />
  <source src="viper.ogg" type="audio/ogg" />
  <p>
    Your browser doesn't support this audio file. Here is a
    <a href="viper.mp3">link to the audio</a> instead.
  </p>
</audio>
```

### 📝 은지
## 이미지

### 이미지 넣는 방법

```html
<img src="https://www.example.com/images/dinosaur.jpg" alt="Dinosaur" />
```

- URL을 사용하는 것은 추천하지 않음
- 사이트에서 사용할 이미지를 호스팅해야함
- 그리고 그냥 유지보수 측면에서 절대 URL보다 상대 URL을 사용하는 것이 더 효율적

### 대체 텍스트

- 이미지가 안뜨면 대신 뜸
- 스크린 리더가 읽을 수 있어 유용하다
- 파일명을 잘못적거나 이름을 잘 못적었을 수도 있음
- 브라우저에서 이미지가 지원이 안되는 사용자자가 있음 → **Lynx**
- 검색 엔진이 활용할 수 있음
- 사용자가 데이터 전송량과 방해 요소를 줄이기 위해서 고의적으로 이미지를 꺼놨을 수 있음

### figure 사용하기

```html
<figure>
  <img
    src="images/dinosaur.jpg"
    alt="The head and torso of a dinosaur skeleton;
            it has a large head with long sharp teeth"
    width="400"
    height="341" />

  <figcaption>
    A T-Rex on display in the Manchester University Museum.
  </figcaption>
</figure>
```

- 이미지나 다이어그램, 차트, 동영상 같은 내용물에 주석이나 캡션을 추가할 때 사용한다

### CSS 배경 이미지

```css
p {
  background-image: url("images/dinosaur.jpg");
}
```

- 임베디드 이미지는 HTML이미지보다 위치 지정과 제어가 훨씬 쉬움
- 스크린리더에 보이지도 않고 텍스트 대체가 없어서 장식으로만 사용할 때 사용해라

## 비디오

HTML 문서에 오디오 및 비디오 컨텐츠를 임베드하기 위해 사용

### 기본 사용법

```html
<video src="myVideo.mp4" controls></video>
```

→ "myVideo.mp4"라는 파일을 웹 페이지에 플레이할 비디오로 임베드하며, 사용자는 비디오를 제어할 수 있는 기본 컨트롤러(재생, 일시정지 등) 봄

### 여러 소스 지원

```html
<video controls>
  <source src="example.mp4" type="video/mp4" />
  <source src="example.webm" type="video/webm" />
  <track kind="subtitles" src="subtitles_es.vtt" srclang="es" label="Spanish" />
</video>
```

- `sorce` : 웹 브라우저마다 지원하는 비디오 형식이 다를 수 있기 때문에, 다양한 비디오 형식의 소스를 제공하여 호환성을 보장할 수 있음
- `track` : 비디오에 자막추가한 거

### 대체 콘텐츠

- `video` 태그 내부에 텍스트나 다른 콘텐츠를 넣을 수 있음. 지원하지 않는 경우에 표시됨

## `<object>` 로부터 `<iframe>`까지 — 기타 임베딩 기술


`<iframe>` 요소는 다른 웹 페이지를 삽입하기 위해, 다른 두 요소는 PDF 파일과 같은 외부 자원을 웹 페이지에 추가하기 위해 사용

### 임베딩의 짧은 역사

1. **초기의 웹**: 웹의 초기 단계에서는 멀티미디어 컨텐츠를 웹 페이지에 직접 포함시키는 기능이 부족, 대신 외부 플러그인 또는 애플리케이션을 사용하여 오디오나 비디오를 재생
2. **플러그인**: 이러한 플러그인들은 컨텐츠를 재생하기 위해 필요했지만, 사용자 경험을 저하시키고 보안 문제를 일으키는 경우도 있음
3. **Flash**: Adobe Flash는 웹에서 멀티미디어 컨텐츠를 임베드하는 가장 인기 있는 도구 중 하나. 그러나 모바일 장치에서의 지원 문제, 보안 이슈, 성능 문제로 인해 점차 사용이 감소
4. **HTML5**: HTML5의 등장으로 **`<audio>`**와 **`<video>`**와 같은 네이티브 태그가 포함되어 웹 개발자들이 쉽게 오디오와 비디오를 임베드할 수 있게 됨. 플러그인의 필요성을 줄이고, 표준화된 방식으로 웹에서 멀티미디어 컨텐츠를 사용가능

### 보안

- iframe이 웹상에서 악의를 품은 사람들의 일반적인 공격 목표가 된다
- 웹페이지를 수정하거나, 사용자 명이나 비밀번호등 정보 유출을 하려고 함

### 규칙

- 필요한 경우에만 삽입해라 → 보안과 관련된 문제들이 많기 때문에
- HTTPS를 사용해라
- 항상 sandbox를 사용해라
    - 웹 사이트를 악용하려는 사람들이 공격할 여지를 최소화하기 위해 콘텐츠에 대해서는 필요한 작업만 허용해야함
    - 다른 코드베이스에 영향을 미치지 않으면서도 특정 코드를 테스트하거나 적절하게 사용할 수 있도록 코드를 감싸고 있는 영역
- CSP(콘텐츠 보안 정책) 지시어를 사용해라
    - HTML 문서 보안을 개선하기 위해 고안된 일련의 HTTP 헤더를 제공

### embed, object

1. **`<object>`**:
    - **`<object>`**는 외부 리소스(예: 이미지, 오디오 클립, Java 애플릿, Flash 애니메이션 등)를 임베드하거나 웹 페이지에 표시하는 일반적인 방법입니다.
    - **`data`** 속성을 사용하여 임베디드할 리소스의 URL을 지정합니다.
    - **`type`** 속성을 사용하여 리소스의 MIME 타입을 지정할 수 있습니다.
    - **`<object>`** 내부에 넣은 콘텐츠는 오브젝트가 로드되지 않았을 때 보여집니다 (폴백 콘텐츠).
    
2. **`<embed>`**:
    - **`<embed>`**는 비슷한 용도로 사용되지만, 오래된 브라우저에서 주로 사용되었습니다.
    - **`src`** 속성을 사용하여 임베디드할 리소스의 경로를 지정합니다.
    - 최근의 웹에서는 **`<object>`**나 다른 방법을 사용하는 것이 권장됩니다.

## 벡터 그래픽 추가하기

### 장점

- 크기 조절 가능: 확대 및 축소 시 품질저하 없음
- 파일 크기 : 일반적으로 비트맵 이미지보다 작음
- 수정 용이 : 코드나 소프트웨어로 쉽게 수정 가능

### svg

- 웹에서 벡터 그래픽을 표현하기 위한 XML 기반의 포맷
- 직접 HTML 내에 포함하거나 외부 파일로 링크하여 사용가능
- CSS와 JS로 스타일 및 상호작용을 적용할 수 있음

### img태그로 SVG 사용

장점

- a 태그 안에 img 태그 중첩해서 이미지를 하이퍼링크로 만들 수 있음
- SVG파일을 브라우저에서  캐시할 수 있어서 나중에 로드된 이미지를 사용하는 모든 페이지의 로딩 시간이 빨라짐

단점

- JS로 이미지 조작 못함
- SVG 코드에 인라인 CSS를 추가해서 스타일링 해야됨

### **HTML 내 SVG 사용**

- **`<svg>`**  태그를 사용하여 웹 페이지에 직접 벡터 그래픽을 추가할 수 있음.

장점

- HTML 인라인에 추가하면 HTTP 요청이 절약되므로 로딩 시간을 조금 줄일 수 있음
- a 태그로 감싸서 하이퍼링크로 만들 수 있음
- CSS 상호작용 가능(:focus)

단점 

- SVG를 한 곳에서만 사용하는 경우에 적합함
- 추가 SVG코드는 HTML의 크기를 증가 시킴
- 인라인 SVG를 캐시할 수 없으므로 이미지가 포함된 첫 페이지가 로드된 후에는 이미지가 포함된 페이지가 더 빨리 로드되지 않음

## 반응형 이미지

```html
<picture>
  <source media="(max-width: 799px)" srcset="elva-480w-close-portrait.jpg" />
  <source media="(min-width: 800px)" srcset="elva-800w.jpg" />
  <img src="elva-800w.jpg" alt="딸 엘바를 안고 서 있는 크리스" />
</picture>
```

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
