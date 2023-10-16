## 3.7 Backgrounds and borders

### 📝 나연

#### 배경 이미지

```css
.a {
  background-image: url(balloons.jpg);
}
```

#### 배경 이미지 반복 제어

```css
// 배경 반복 X
background-repeat: no-repeat;
// 수평으로 반복
background-repeat: repeat-x;
// 수직으로 반복
background-repeat: repeat-y;
// 양방향으로 반복 [기본값]
background-repeat: repeat;
```

#### 배경 이미지 크기

`background-size`

cover : 브라우저는 이미지를 박스 면적을 완전히 덮으면서 가로 세로 비율을 유지하며 이미지를 충분히 크게 만듬. 이 경우 일부 이미지가 박스 외부에 있을 수 있다.

contain — 브라우저는 이미지를 박스 안에 들어가기에 적합한 크기로 만듬.

#### 배경 이미지 위치

`background-position`

```css
background-position: top center;
background-position: top 20px;
background-position: 20px 10%;
```

다양하게 혼합가능

#### 여러가지 배경 이미지도 가능

```css
background-image: url(image1.png), url(image2.png), url(image3.png),
  url(image1.png);
background-repeat: no-repeat, repeat-x, repeat;
background-position: 10px 20px, top right;
```

### 테두리

```css
.box {
  border-width: 1px;
  border-style: solid;
  border-color: black;
}

// 스타일 지정도 가능
border-bottom-style: dashed;
```

### 📝 은지

### 📝 정준

### 📝 주현
