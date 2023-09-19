## 2.5 Links

### 📝 나연

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

### 📝 주현
