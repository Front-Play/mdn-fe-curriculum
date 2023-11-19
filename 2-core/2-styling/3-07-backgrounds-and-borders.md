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
**background-size**

- cover — 브라우저는 이미지를 박스 면적을 완전히 덮으면서 가로 세로 비율을 유지하며 이미지를 충분히 크게 만듭니다. 이 경우 일부 이미지가 박스 외부에 있을 수 있습니다.
- contain — 브라우저는 이미지를 박스 안에 들어가기에 적합한 크기로 만듭니다. 이 경우 이미지의 종횡비가 박스의 종횡비와 다른 경우, 이미지의 한쪽 또는 위쪽과 아래쪽에 간격이 생길 수 있습니다.

웹 성능, 배경 색상 대비
https://juicystudio.com/services/luminositycontrastratio.php#specify


**border-radius**

```css
.box {
  border-top-right-radius: 1em 10%;
}
```

### 📝 정준

### Background

CSS를 통해 배경을 지정할 수 있습니다. 다음 속성을 사용해 배경을 지정하고 설정합니다.

- `background-image`: url 설정
  - e.g. `background-image: url(이미지 주소)`
- `background-size`: 배경의 이미지 크기 조정
  - `cover`: 박스 면적을 완전히 덮도록 설정(이미지의 가로세로 비율은 유지됩니다), 이 경우 이미지가 박스 바깥으로 벗어나 잘릴 수 있음
  - `contain`: 박스에 들어가기 적당한 크기로 조정, 이때 **이미지의 종횡비**와 **박스의 종횡비**가 다를 수 있음
- `background-color`: 배경색 설정
- `background-repeat`: 이미지 반복 제어
  - `no-repeat`: 배경이 반복되지 않도록 설정
  - `repeat-x`: 수평으로 반복
  - `repeat-y`: 수직으로 반복
  - `repeat`: 기본값; 양방향으로 반복

<br/>

#### 배경 이미지 배치

배경 이미지에도 position을 설정할 수 있습니다.

- `background-position`: x값, y값 순으로 작성
  - `top`, `left`와 같은 키워드도 사용 가능합니다.

```css
/* 키워드 사용 */
.box {
  background-image: url(star.png);
  background-repeat: no-repeat;
  background-position: top center;
}

/* 백분율, 길이 값 지정 */
.box {
  background-image: url(star.png);
  background-repeat: no-repeat;
  background-position: 20px 10%;
}
```

> 값을 x, y축에서 어떤 방향으로 값을 지정하는지 디테일한 설정이 가능합니다.  
> 이때 길이 단위는 앞에 오는 값과의 offset입니다.
>
> ```css
> .box {
>   background-image: url(star.png);
>   background-repeat: no-repeat;
>   background-position: top 20px right 10px;
> }
> ```

### Border

테두리 속성을 일컫으며 하나씩 작성하기도, 한번에 작성하기도 가능하다.

```css
/* 한번에 작성 */
.box {
  border: 1px solid black;
}

/* 나눠서 작성 */
.box {
  border-width: 1px;
  border-style: solid;
  border-color: black;
}
```

<br/>

#### 특정 방향 border 지정

또한 특정 방향에만 border를 주는 것도 가능하다.  
이는 `-`뒤에 원하는 방향을 명시한다.

```css
.box {
  border-top: 1px solid black;
  border-bottom: 3px solid blue;
  border-left: 2px solid red;
  border-right: 1px dotted yellow;
}
```

> 참고: `longhands`
>
> ```css
> .box {
>   border-top-width: 1px;
>   border-top-style: solid;
>   border-top-color: black;
> }
> ```

<br/>

#### 둥근 테두리

```css
.box {
  border-radius: 10px;
}

.box {
  border-top-right-radius: 1em 10%;
}
```

### 📝 주현
