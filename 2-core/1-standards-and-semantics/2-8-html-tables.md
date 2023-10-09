## 2.8 HTML tables

### 📝 나연

```html
<tr>
  <td>Hi, I'm your first cell.</td>
  <td>I'm your second cell.</td>
  <td>I'm your third cell.</td>
  <td>I'm your fourth cell.</td>
</tr>
```

4개의 셀 / 한개의 행

td 태그만으로 테이블을 구성할 수 있지만, th 태그 적극 추천!

테이블의 구조가 복잡해지면 ` <thead>, <tfoot>, <tbody>` 를 사용하여 구조 추가하는 것도 방법

### 📝 은지
#### 기본 개념

테이블은 그리드 형식의 데이터를 표현하기 위해 사용됩니다.
행과 열로 구성되어 데이터를 정렬합니다.
#### 테이블 생성 요소

- `<table>`: 테이블의 시작과 끝을 정의합니다.
- `<tr>`: 테이블의 각 행을 정의합니다.
- `<td>`: 테이블 데이터 셀을 정의합니다. 각 셀은 특정 정보나 데이터를 포함합니다.
- `<th>`: 테이블 헤더 셀을 정의합니다. 일반적으로 열 또는 행의 제목을 나타냅니다.
#### 테이블 구조

- `<thead>`: 테이블의 헤더 섹션을 그룹화합니다.
- `<tbody>`: 주요 테이블 콘텐츠를 그룹화합니다.
- `<tfoot>`: 테이블의 바닥글 섹션을 그룹화합니다.
#### 테이블 셀의 속성

- `colspan`: 셀이 여러 열을 차지하도록 합니다.
- `rowspan`: 셀이 여러 행을 차지하도록 합니다.
#### 테이블 접근성

- `<caption>`: 테이블에 대한 설명 또는 캡션을 제공합니다.
- `scope`: 헤더 셀(<th>)이 어느 행 또는 열에 적용되는지 나타냅니다, 테이블 접근성을 향상시키기 위해 사용됩니다.


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
