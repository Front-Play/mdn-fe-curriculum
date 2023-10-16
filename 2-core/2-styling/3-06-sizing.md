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

### 📝 정준

### 📝 주현
