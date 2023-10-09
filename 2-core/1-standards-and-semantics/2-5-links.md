## 2.5 Links

### 📝 나연

웹을 웹답게 만든다! 에서 하이퍼 링크는 중요!
하이퍼링크를 사용하면 문서를 다른 문서나 리소스에 연결 / 문서의 특정 부분에 연결 / 웹 주소에서 앱을 사용할 수 있다.

어떤 내용이든 link 로 변경가능 -> block level!
`<a>` 태그로 감싸자~

### 📝 은지
### 하이퍼 링크

- 문서를 다른 문서나 리소스에 연결하거나, 문서의 특정 부분에 연결하거나, 웹 주소에서 앱을 사용할 수 있음
- 클릭하거나 다른 방법으로 활성화된 웹 브라우저가 다른 웹 주소로 이동하도록 거의 모든 웹 콘텐츠를 링크로 변환할 수 있음

### 링크 구조

```jsx
<p>
	 <a href="https://www.mozilla.org/en-US/" 
			title="The best place to find more information about Mozilla's">
					Mozilla 홈페이지 </a> 로 향하는 링크를 만들었습니다.
</p> 
```

- `[<a>](https://developer.mozilla.org/ko/docs/Web/HTML/Element/a)` 요소 안에 감싸고 웹 주소를 포함하는 `[href](https://developer.mozilla.org/ko/docs/Web/HTML/Element/a#href)` 속성(**Hypertext Reference** 또는 **target**)을 사용하여 생성
- 안에 태그를 넣어서 블록 레벨로 만들 수 있음
- `title`  속성은 페이지에 포함된 정보 또는 웹 사이트에서 주의해야 할 사항 등 추가정보 포함하고 있음

### path로 작성하는 경우

```jsx
<p>나의 <a href="../pdfs/project-brief.pdf">프로젝트 개요</a> 링크입니다.</p>
```

### 링크명은 확실하게 적을 것

```jsx
// ✅
<p><a href="https://www.mozilla.org/firefox/">Download Firefox</a></p>

// ❎
<p>
  <a href="https://www.mozilla.org/firefox/">Click here</a> to download Firefox
</p>
```

- 스크린 리더 사용자, 검색엔진, 시각적 독자 관점

### 기타 팁

- 링크 텍스트는 가능한 짧게 작성하기
- 동일한 텍스트의 여러 복사본이 서로 다른 장소에 연결되는 경우 최소화 하기 → “여기 클릭”
- 링크 텍스트에 "link"나 "links to"라고 쓰지말기
- 링크를 눌러서 문서가 다운로드되는 경우는 명확히 나타내기 → `download` 속성 사용하기
- 이메일 링크를 보낼때는 `href`안에 “`mailto:`" 넣기

### 📝 정준

### 하이퍼 링크 설정하기

> **하이퍼링크란?**: 문서를 다른 문서 또는 리소스, 앱 등으로 연결 시키는 것

- `<a>`: 하이퍼링크를 연결 시키는 태그

  - `href`: 어떠한 곳으로 연결시킬지 설정하는 속성
  - `title`: 마우스를 hover했을 때 나타낼 설명을 설정하는 속성

- 하이퍼 링크는 일반 테스트 부터 block요소, 이미지까지 모든 html요소에 연결할 수 있다.

  - 예시:

  ```html
  <p>
    I'm creating a link to
    <a
      href="https://www.mozilla.org/en-US/"
      title="The best place to find more information about Mozilla's
          mission and how to contribute"
    >
      the Mozilla homepage</a
    >.
  </p>
  ```

### URL과 Path

1. `URL`: 단순히 무언가가 웹상의 어디에 위치하는지 결정하는 하나의 텍스트 문자열
2. `path`: 관심있어 하는 파일이 파일 시스템 어디에 있는지 구체적으로 명시

- URL은 파일들을 찾기위해 path를 이용한다.
- 프로젝트 내 파일 경로 외에 다른 웹 URL을 연결할 수도 있다.

#### 문서 조각 연결

- 작성한 문서 요소에서 지정한 특정 지점에도 연결할 수 있다.
  - 지정한 요소
  ```html
  <h2 id="Mailing_address">Mailing 주소</h2>
  ```
  - 문서 조각에 연결
  ```html
  <p>
    우리에게 메일을 보내고 싶나요? 그럼
    <a href="contacts.html#Mailing_address">메일 주소</a>를 확인해주세요.
  </p>
  ```

### 절대경로와 상대경로

1. **절대경로**: 웹에서 지정되어 있는 경로를 일컫는다. 어디서든 절대경로로 연결하면 미리 지정해둔 경로로 연결된다.

2. **상대경로**: 연결을 시키는 파일과의 상대적인 위치를 가르키는 경로이다.

### 비 HTML소스를 연결할 경우?

- `비HTML소스`를 연결할 경우 해당 링크의 목적을 명확히 알 수 있도록 명기해야 한다.
- ```html
  <a href="https://www.example.com/large-report.pdf">
    Download the sales report (PDF, 10MB)
  </a>
  ```

### 속성 사용하기

#### 1) 다운로드 링크 연결 시 `donwload`속성 상용

```html
<a
  href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=en-US"
  download="firefox-latest-64bit-installer.exe"
>
  Download Latest Firefox for Windows (64-bit) (English, US)
</a>
```

#### 2) 이메일 연결

```html
<a href="mailto:nowhere@mozilla.org">아무데나 전자 메일 보내기</a>
```

### 📝 주현
