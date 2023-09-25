## 3.3 The box model

### 📝 나연

CSS 에 포함되는 모든 요소를 감싸는 것은 Box!

#### 블록

상자가 새 줄로 나뉨
너비 및 높이 속성은 그대로 유지.
패딩, 마진 및 보더를 사용하면 다른 요소가 상자에서 밀려남.
너비를 지정하지 않으면 상자가 인라인 방향으로 확장되어 컨테이너의 사용 가능한 공간을 채운다! 대부분의 경우 상자는 컨테이너만큼 넓어져 사용 가능한 공간의 100%를 채움!

#### 인라인

상자가 새 줄 X
너비 및 높이 속성이 적용 X
위쪽 및 아래쪽 패딩, 마진 및 보더는 적용되지만 다른 인라인 상자가 상자에서 멀어지지는
왼쪽 및 오른쪽 패딩, 마진 ,보더가 적용되며 다른 인라인 상자가 상자에서 멀어지게 됩니다.

우리는 `flex` / `display` 값을 사용하여 내부 디스플레이 유형을 변경할 수 있다!

#### Box-Sizing

```css
/* 테두리를 기준으로 크기를 정한다!  */
box-sizing: border-box;
```

만약 아래와 같은 box 가 있다면,

```css
.box {
  width: 350px;
  height: 150px;
  margin: 25px;
  padding: 25px;
  border: 5px solid black;
}
```

표준 박스 모델을 사용하여 박스가 차지하는 공간은 실제로 너비 410px(350 + 25 + 25 + 5 + 5), 높이 210px(150 + 25 + 25 + 5 + 5)가 된다! 왜냐면 양쪽 패딩과 테두리는 콘텐츠 박스에 사용되는 width 에 더해지기 때문!

근데 개발자 입장에서 테두리와 패딩을 추가한 width 와 height 가 불편하다고 느낄 수 있다! 그래서 Box-Sizing 를 사용하면 원하는 방향성으로 width / height 의 기준을 정할 수 있음!

### 여백에 관해

```css
.one {
  margin-bottom: 50px;
}

.two {
  margin-top: 30px;
}
```

```html
<div class="container">
  <p class="one">I am paragraph one.</p>
  <p class="two">I am paragraph two.</p>
</div>
```

이렇게 이싿면 중간에 여백이 80px 일것같지만! 50이다!

이것이 여백 축소현상!

인라인 요소에 패딩을 적용하고 싶다면..

```css
display: inline-block;
```

을 사용하자!

### 📝 은지

### 📝 정준

### 📝 주현
