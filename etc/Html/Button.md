

## div
```html
<div
  role="button"
  tabindex="0"
  onclick="handleClick()"
  onkeydown="handleKeyDown(event)"
  style="cursor: pointer;"
>
  Click me
</div>
```

role="button"	
- 스크린 리더 등 보조기기에 이 요소가 버튼임을 알려줍니다.

tabindex="0"	
- 키보드 포커스로 이동할 수 있게 합니다. (-1이면 키보드 포커스 안됨)

onkeydown="..."	
- 스페이스바/엔터키로도 눌릴 수 있도록 처리합니다.


```js
function handleKeyDown(event) {
  if (event.key === "Enter" || event.key === " ") {
    event.preventDefault(); // 스페이스바는 기본 스크롤을 막아야 함
    handleClick();
  }
}

function handleClick() {
  alert("Button clicked!");
}
```

결론
- button >> div



## CursorPointer
button
- ❌cursor: pointer;
- 추가필요