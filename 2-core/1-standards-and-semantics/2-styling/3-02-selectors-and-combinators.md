## 3.2 Selectors and combinators

### 📝 나연

### 📝 은지
## 선택자 목록

```css
h1 {
  color: blue;
}

.special {
  color: blue;
}
```

```css
h1, .special {
  color: blue;
}
```

```css
h1,
.special {
  color: blue;
}
```

## 유형, 클래스 및 ID 선택자

| HTML 요소 | h1 {} |
| --- | --- |
| 클래스 | .box {} |
| ID | #unique {} |

## 속성 선택자

그룹은 요소에 특정 속성이 있는지에 따라 요소를 선택

```css
a[title] {
}
```

특정 값을 가진 속성의 존재 여부에 따라 선택할 수 있음

```css
a[href="https://example.com"]
{
}
```

## 의사 클래스 및 의사 요소

요소 자체가 아닌 요소의 특정 부분을 선택하는 의사 요소도 포함

```css
p::first-line {
}
```

## 결합자

하위 결합자

```css
article > p {
}
```


### 📝 정준

### 📝 주현
