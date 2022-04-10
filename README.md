## 노마드코더- React.JS 강의에 대한 공부내용을 기록하고 있습니다.
```js
// 자바스크립트에서 함수를 선언하는 방법들
// 보통은 첫번째, 두번째를 대부분 사용한다.

// named function declaration
function hello() {
  ...
}

// anonymous function expression
let hello = function () {
  ...
}

// named function expression

let hello = function originalName() {
  ...
}

// arrow function
let hello = () => {
  ...
}

```
### What is React.js?
JS 라이브러리이며, 기본적으로 element간 상호작용을 매우 간편하게 구현하게 해준다.
HTML, CSS, JS로만 구현시 HTML => JS 로 작성하는 순서이나, React.js는 JS => HTML render 순서로 진행됨



### React.JS가 필요한 이유?
HTML, CSS, JS로만 코드를 작성시에, 단순히 버튼 클릭수를 측정하는 기능을 구현하는데만 아래와 같은 코드양이 필요하다
1. 태그 선택
2. 선택한 태그에 대한 이벤트 리스너 설정
3. 콜백함수를 구현. 선택한 태그에 대해 조작할 데이터 설정
4. HTML 태그 업데이트 (.innerText 나 속성을 변경해주는 등..)
```html
<!DOCTYPE html>
<html lang="en">
<head>
</head>
<body>
  <span id="test-span">Total Click: 0</span>
  <button id="test-btn">Click Me</button>
  <script>
    let counter = 0;
    const button  = document.querySelector("#test-btn");
    const span = document.querySelector("#test-span");

    function handleClick() {
      console.log("클릭클릭!")  
      counter = counter + 1;    
      // 특정 태그 내부의 text를 변경할때 .innerText 사용
      span.innerText = `Total Click: ${counter}`
    }


    button.addEventListener("click", handleClick);
  </script>
</body>
</html>
```