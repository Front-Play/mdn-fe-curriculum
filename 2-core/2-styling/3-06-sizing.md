## 3.6 Sizing

### 📝 나연

빈 div 에는 width, height 값이 없음.

#### min- / max- 크기

container 크기에 맞게 늘어남.

`max-width: 100%` : 이미지가 고유 크기보다 작아질 수 있지만, 크기의 100%에서 멈춤.

#### Viewport 단위

1vh = viewport 높이의 1%
1wh = viewport 너비의 1%

#### 텍스트 표시 방향 제어

1. 쓰기 모드

```css
writing-mode: horizontal-tb;
// 가로
writing-mode: vertical-rl;
// 오른쪽에서 왼쪽으로 -> 문장은 수직
writing-mode: vertical-lr;
// 왼쪽에서 오른쪽으로 -> 문장은 수직
```

2. 쓰기 모드와 블록 및 인라인 레이아웃

블록 크기는 항상 쓰기 모드에서 페이지에 표시되는 방향 블록
인라인 크기는 항상 문장이 표시되는 방향

```css
.box {
  inline-size: 200px;
  writing-mode: vertical-rl;
}
```

(여기 예제 참고)

https://developer.mozilla.org/ko/docs/Learn/CSS/Building_blocks/Handling_different_text_directions#%EB%85%BC%EB%A6%AC%EC%A0%81_%EA%B0%92

### 📝 은지
 - Min-Width와 Min-Height: min-width와 min-height 속성을 사용하여 요소의 최소 크기를 설정
 - Max-Width와 Max-Height: max-width와 max-height 속성을 사용하여 요소의 최대 크기를 설정
 - 백분율 단위: 백분율 단위를 사용하여 상위 요소의 크기에 대한 비율로 크기를 지정
 - Viewport 단위: vw, vh, vmin, vmax와 같은 viewport 단위를 사용하여 뷰포트 크기에 대한 비율로 크기를 지정
 - Flexbox와 Grid 레이아웃: Flexbox와 Grid 레이아웃을 사용하여 요소 간 크기와 위치를 관리
 - Auto 값: 일부 속성에 auto 값을 지정하면 브라우저가 요소의 크기를 자동으로 계산

### 📝 정준

### CSS로 Sizing

#### 1. 기본 사이즈

- 본질적으로 HTML요소는 CSS영향을 받기 전엔 자연스러운 본래의 크기(고유 크기, intrinsic size)를 지닌다.

> But!! 빈 `div`태그는 자체 크기가 없다.
>
> - `width`는 100%이지만 `height`이 없음

---

<br/>

#### 2. Size 설정

- CSS를 통해 사이즈를 설정할 수 있습니다. 이때 설정한 크기보다 컨텐츠가 많아지면 해당 내용은 설정된 높이로 인해 `overflow`하게 됩니다.
- `width`와 `height`, `margin`과 `padding` 모두 백분율을 사용해 크기를 지정할 수 있습니다.

---

<br/>

#### 3. max-, min-

`width`와 `height` 앞에 `min-` 또는 `max-`를 접두어로 붙여 **최소 크기**와 **최대 크기**를 지정할 수 있습니다.

- `min-width` & `min-height`: 최소 너비와 최소 높이
- `max-width` & `max-height`: 최대 너비와 최소 높이

#### 3-1. 최소 높이(min-height) 설정으로 인한 영향

- `min-height`를 설정하면 안의 컨텐츠가 많아질 수록 박스의 높이가 증가합니다.
- 이를 통해 overflow되는 것을 막고, 컨텐츠에 맞춰 높이를 증가시킬 수 있습니다.

> overflow 를 피하면서 가변적인 양의 콘텐츠를 처리할 때 매우 유용

#### 3-2. 최대 너비(max-width) 설정으로 인한 영향

- `max-width`설정을 통해 이미지를 가변적으로 조정되도록 맞추기 용이합니다.
  - 만일 공간이 이미지의 원래 크기를 나타낼 정도로 충분치 않으면 이미지가 크기에 맞춰져 줄여집니다.
  - 또한 이와 동시해 설정한 너비보다 커지지 않게 합니다.

---

<br/>

#### 4. viewport 단위

- `vw`: view-width로써 너비를 지정
- `vh`: view-height로써 높이를 지정

변경되는 viewport에 맞춰 박스의 크기도 조절됩니다.

<br/>

### 📝 주현
