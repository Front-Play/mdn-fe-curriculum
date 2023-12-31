## 3.8 Overflow

### 📝 나연

CSS 는 내용을 숨기지 않기 때문에
안에 콘텐츠가 컨테이너에서 넘치는 경우가 발생.

#### overflow 속성

기본값은 `visible`
`overflow: hidden` 을 하면 콘텐츠가 넘칠때 숨길 수 있음  
`overflow: scroll` : 스크롤 막대 무조건 추가  
`overflow: auto` : 스크롤 막대를 표시해야할 경우에만 추가됨  
`overflow-y: scroll` : y축에서만 스크롤할 수 있음  
`overflow-x: scroll` :
x축에서만 스크롤할 수 있지만, 긴 단어를 처리하는 데 권장되는 방법은 아님.   

작은 박스에서 긴 단어를 처리해야하는 경우 `word-break` or `overflow-wrap` 속성을 사용하는 것이 좋음

### 📝 은지
- scroll 또는 auto 와 같은 overflow 값을 사용할 때 BFC 를 생성한다는 것을 아는 것이 유용합니다. 결과적으로 overflow 값을 변경한 박스의 내용이 자체의 미니 레이아웃이 됩니다.

### 📝 정준

### Overflow란?

CSS는 기본적으로 데이터 손실을 줄이고자 한다. 그래서 박스의 컨텐츠가 설정한 너비(width)와 높이(height)를 초과하더라도 그대로 표현한다.

이는 데이터 손실을 줄여 사용자가 모르는 정보가 있지 않게 하기 위해서이다.  
그러나 이때 우리는 `overflow`란 속성을 이용해 이를 조절할 수 있다.

#### 1. hidden

넘치는 정보를 숨깁니다. 사용자는 이 정보가 가려지거나 사라진 것처럼 보입니다.

```CSS
.box {
  overflow: hidden;
}
```

#### 2. scroll

넘치는 정보를 숨기지만 스크롤을 통해 사용자가 볼 수 있도록 합니다.

- 단, scroll할 정보가 없더라도 스크롤 바가 나타나게 됩니다.

```CSS
.box {
  overflow: scroll;
}
```

특정 방향에만 스크롤이 생기도록 지정하는 것 또한 가능합니다.

```css
.box-x {
  overflow-x: scroll;
}

.box-y {
  overflow-y: scroll;
}
```

#### 3. auto속성

이 속성을 사용하면 넘치는 상황을 감지하여 자동으로 스크롤을 생성해주고, 그렇지 않을 때는 스크롤을 보이지 않습니다.

```CSS
.box {
 overflow: auto;
}
```

### 📝 주현
