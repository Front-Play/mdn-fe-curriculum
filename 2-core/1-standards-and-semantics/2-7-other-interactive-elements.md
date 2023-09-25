## 2.7 Other interactive elements

### 📝 나연

```tsx
<label>
  Please choose one or more pets:
  <select name="pets" multiple size="4">
    <optgroup label="4-legged pets">
      <option value="dog">Dog</option>
      <option value="cat">Cat</option>
      <option value="hamster" disabled>
        Hamster
      </option>
    </optgroup>
    <optgroup label="Flying pets">
      <option value="parrot">Parrot</option>
      <option value="macaw">Macaw</option>
      <option value="albatross">Albatross</option>
    </optgroup>
  </select>
</label>
```

아직 `<optgroup>` 태그는 한번도 안 써봐서 새롭네요...!!

### 📝 은지
다양한 속성들이 있다..
#### 기본적인 폼 구조

- `<form>`: 폼의 시작과 끝을 나타냅니다. action 속성은 데이터를 처리할 서버 측 URL을 지정합니다.
- `method`: 데이터를 서버로 보내는 방식 (GET 또는 POST).
  
#### 입력 요소

- `<input>`: 다양한 유형의 입력 데이터를 받을 수 있습니다 (text, password, radio, checkbox 등).
- `<textarea>`: 여러 줄의 텍스트 입력에 사용됩니다.
- `<select>`: 드롭다운 선택 목록을 만듭니다. `<option>` 태그와 함께 사용됩니다.
- `<button>`: 사용자가 클릭할 수 있는 버튼을 생성합니다.
#### 입력 타입 및 속성

- `type`: 입력의 종류를 정의합니다 (예: text, email, date).
- `placeholder`: 입력 필드 내에 힌트 또는 설명을 표시합니다.
- `required`: 입력 필드가 필수적인지 나타냅니다.
- `pattern`: 입력 값의 형식을 정의하는 정규 표현식을 제공합니다.
### 📝 정준

### 📝 주현
