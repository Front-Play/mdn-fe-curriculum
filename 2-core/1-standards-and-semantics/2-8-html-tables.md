## 2.8 HTML tables

### 📝 나연

### 📝 은지

### 📝 정준

### Table 만들기

#### 1. Table의 구조

HTML에서 테이블 구조를 만들고자 할 때 `<table>`태그를 사용하며, 안의 구성요소는 다음과 같다.

- `<tr>`: row(행)를 뜻 한다.
  - `<th>`: 테이블 행과 열의 title을 나타낸다.
  - `<td>`: 테이블 cell의 내용을 담는다.

#### 2. 추가 디테일

추가적으로 테이블을 디테일하게 분리할 수 있는 태그는 다음과 같다.

- `<thead>`: 테이블 헤더
- `<tbody>`: 테이블 바디(컨텐츠)
- `<tfoot>`: 테이블 푸터
- `<caption>`: 테이블의 짧은 설명을 나타낸다.

> [테이블의 고급 기능 알아보기](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Advanced)
>
> - 위 링크에서 테이블 관련 태그에서 사용하는 속성(`property`)도 확인 가능하다.

#### ➕) 통합 예시:

```html
<table>
  <caption>
    Council budget (in £) 2018
  </caption>
  <thead>
    <tr>
      <th>Items</th>
      <th scope="col">Expenditure</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Donuts</th>
      <td>3,000</td>
    </tr>
    <tr>
      <th scope="row">Stationery</th>
      <td>18,000</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th scope="row">Totals</th>
      <td>21,000</td>
    </tr>
  </tfoot>
</table>
```

> **셀 병합하기**
>
> - `rowspan`: 열을 병합
> - `colspan`: 행을 병합

### 📝 주현
