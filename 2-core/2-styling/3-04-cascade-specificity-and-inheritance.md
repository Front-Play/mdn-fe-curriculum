## 3.4 Cascade, specificity, and inheritance

### 📝 나연

CSS = Cascading Style Sheets

#### cascade

규칙의 순서가 중요하다.
동일한 우선순위를 가질 때는 마지막에 정의된 규칙이 사용됨.

#### Inheritance

부모 요소에서 설정된 **일부** CSS 속성 값은 자식 요소에 의해 상속!

✅ Controlling inheritance

```css
/*  부모 요소의 속성 값과 동일하게 설정 */
color: inherit;
/* 부모 요소와 상관없이 초기값 설정 */
color: initial;
/* 기본 스타일로 재설정 
 부모 속성으로 돌아가거나 부모가 없을 때는 최초의 상태로 돌아감
*/
color: revert;
/* 부모로부터 상속할 값이 있으면 상속값 = inherit or 없으면 초깃값을 사용함 = initial */
color: unset;
```

initial 예시

```html
<p>
  <span>This text is red.</span>
  <em>This text is in the initial color (typically black).</em>
  <span>This is red again.</span>
</p>
```

```
p {
  color: red;
}

em {
  color: initial;
}
<!-- 그럼 p태그에 하위에 있는 span 태그만 color : red! -->
```

#### !important

모든 규칙 무시

### 상속 선택자

### 📝 은지

### 📝 정준

### 📝 주현
