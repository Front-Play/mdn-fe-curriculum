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
1. **계단식(Cascade):**
    - CSS는 '계단식 스타일 시트'라는 이름에서 알 수 있듯이 '계단식'을 통해 스타일을 결정
    - 여러 스타일 규칙이 하나의 요소에 적용될 경우, 계단식 규칙을 통해 어느 규칙이 최종적으로 적용될지 결정
2. **스타일 결정 순서:**
    - 원천(브라우저의 기본 스타일), 사용자 스타일시트, 개발자 스타일시트 순으로 적용
    - 중요성, 명시성, 소스 순으로 우선순위가 결정
3. **상속(Inheritance):**
    - 상속은 부모 요소의 특정 스타일이 자식 요소에게 전달되는 속성
    - 모든 CSS 속성이 상속되는 것은 아닙니다. 예를 들면, **`background-color`**나 **`border`**는 기본적으로 상속되지 않음
4. **계단식과 상속의 조합:**
    - 상속된 값을 재정의하기 위해, 요소 자체에 스타일을 직접 지정할 수 있음
    - 이러한 재정의는 계단식 규칙에 따라 적용
5. **전역 값(Global values):**
    - 모든 CSS 속성은 **`inherit`**, **`initial`**, **`unset`**, **`revert`** 같은 전역 값을 사용할 수 있습니다. 이러한 값은 특정 속성에 대한 기본값이나 상속 값을 설정하는 데 사용

### 📝 정준

### 📝 주현
