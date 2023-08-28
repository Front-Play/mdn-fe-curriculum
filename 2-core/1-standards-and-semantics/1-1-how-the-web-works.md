## 1.1 How the web works

🔗 https://github.com/mdn/curriculum/blob/main/curriculum/2-core/1-standards-and-semantics/1-1-how-the-web-works.md

### 📝 나연

### 브라우저에 웹 주소를 입력하면 ?

1. 브라우저는 DNS 서버로 이동 -> 실제 주소를 찾는다.
2. 브라우저는 서버에 HTTP 요청 메시지를 보내 웹 사이트의 사본을 클라에게 보내도록 요청. 이때 TCP/IP 사용
3. 서버가 클라 요청을 승인한다는 의미로 200 OK! 메시지 전송 후 데이터 패킷을 전송
4. 브라우저는 데이터 패킷을 모아서 사용자에게 표시

### 컴포넌트 파일이 구분문석되는 순서

1. 브라우저는 HTML 파일을 분석해서 외부 CSS와 자바스크립트 파일을 참조.
2. 파일들을 서버에서 가져와 구문 분석한 후, 인메모리 DOM 트리와 CSSOM 구조를 생성하며 자바스크립트를 실행
3. 페이지의 시각적 내용이 화면에 표시되어 사용자가 상호 작용할 수 있게 됨!

### URL 이란 ?

https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL/mdn-url-all.png

Scheme : 브라우저가 리소스를 요청할 때 사용해야하는 프로토콜 -> HTTPS / HTTP (qlqhdks)

Authority
Path to resource
Parameters : 웹 서버에 제공되는 추가 파라미터. & 기호로 구분된 키/값 쌍의 목록

Anchor : 북마크 지점 ex) git

### 📝 은지

### 📝 정준

### 📝 주현
