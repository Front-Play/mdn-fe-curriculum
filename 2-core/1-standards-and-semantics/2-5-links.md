## 2.5 Links

### 📝 나연

### 📝 은지

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
