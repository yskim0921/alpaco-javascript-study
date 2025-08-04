# 자바스크립트 강의 자료

---

# 1. 자바스크립트 기본 환경 설치 및 기본 문법

- **이론**
    - 자바스크립트란?
    - 개발 환경 구성 (브라우저 + VS Code + Live Server)
    - `<script>` 태그의 위치와 동작
- **실습**
    - HTML에 JS 연결하기
    - 콘솔에 "Hello, JavaScript!" 출력하기
    - 주석, 변수 선언(let, const)

---

# 2. 연산자와 명령문

- **이론**
    - 산술, 비교, 논리, 대입 연산자
    - 조건문(if, switch)
    - 반복문(for, while, do-while)
- **실습**
    - 사용자 입력을 받아 계산기 만들기
    - 반복문으로 구구단 출력

---

좋습니다! 아래는 **자바스크립트 강의 자료: 2. 연산자와 명령문** 단원의 상세 내용입니다.

학습 목표는 **자바스크립트의 기본 제어 구조와 연산자를 이해하고, 조건/반복문을 활용한 로직 구현 능력을 기르는 것**입니다.

---

### 1. 산술 연산자 (Arithmetic Operators)

| 연산자 | 설명 | 예시 | 결과 |
| --- | --- | --- | --- |
| `+` | 덧셈 | `5 + 3` | `8` |
| `-` | 뺄셈 | `5 - 3` | `2` |
| `*` | 곱셈 | `5 * 3` | `15` |
| `/` | 나눗셈 | `5 / 2` | `2.5` |
| `%` | 나머지 | `5 % 2` | `1` |
| `**` | 제곱 | `2 ** 3` | `8` |

### 2. 비교 연산자 (Comparison Operators)

| 연산자 | 의미 | 예시 | 결과 |
| --- | --- | --- | --- |
| `==` | 값이 같음 | `5 == '5'` | `true` |
| `===` | 값과 타입이 같음 | `5 === '5'` | `false` |
| `!=` | 값이 다름 | `5 != '5'` | `false` |
| `!==` | 값 또는 타입 다름 | `5 !== '5'` | `true` |
| `>` `<` `>=` `<=` | 크기 비교 |  |  |

### 3. 논리 연산자 (Logical Operators)

| 연산자 | 설명 | 예시 | 결과 |
| --- | --- | --- | --- |
| `&&` | 그리고 (AND) | `true && false` | `false` |
| ` |  | ` | 또는 (OR) |
| `!` | 부정 (NOT) | `!true` | `false` |

### 4. 대입 연산자 (Assignment)

| 연산자 | 의미 | 예시 |
| --- | --- | --- |
| `=` | 대입 | `x = 10` |
| `+=` | 더해서 대입 | `x += 5` → `x = x + 5` |
| `-=` | 빼서 대입 | `x -= 5` |
| `*=` `/=` `%=` 등 |  |  |

---

### ✅ 조건문

### 1. `if`, `else if`, `else`

```jsx
let age = 20;

if (age < 13) {
    console.log("어린이입니다.");
} else if (age < 20) {
    console.log("청소년입니다.");
} else {
    console.log("성인입니다.");
}

```

### 2. `switch`

```jsx
let grade = 'B';

switch (grade) {
    case 'A':
        console.log("우수");
        break;
    case 'B':
        console.log("양호");
        break;
    case 'C':
        console.log("보통");
        break;
    default:
        console.log("미정");
}

```

---

### 🔁 반복문

### 1. `for`

```jsx
for (let i = 1; i <= 5; i++) {
    console.log(i);  // 1부터 5까지 출력
}
```

### 2. `while`

```jsx
let i = 1;
while (i <= 5) {
    console.log(i);
    i++;
}
```

### 3. `do...while`

```jsx
let i = 1;
do {
    console.log(i);
    i++;
} while (i <= 5);
```

---

### 🧪 실습 과제

### 실습 1: 사용자 입력을 받아 계산기 만들기

**기능 설명**

- 사용자로부터 숫자 2개와 연산자를 입력받아 결과를 출력
- if 또는 switch문 사용

**예시 코드 (prompt 사용)**

```html
<script>
let num1 = Number(prompt("첫 번째 숫자 입력"));
let op = prompt("연산자 입력 (+, -, *, /)");
let num2 = Number(prompt("두 번째 숫자 입력"));
let result;

switch (op) {
    case '+': result = num1 + num2; break;
    case '-': result = num1 - num2; break;
    case '*': result = num1 * num2; break;
    case '/': result = num1 / num2; break;
    default: result = "지원하지 않는 연산자입니다.";
}

alert("결과: " + result);
</script>
```

### 실습 2: 반복문으로 구구단 출력

**예시 코드: for문을 사용하여 2단부터 9단까지 출력**

```jsx
for (let dan = 2; dan <= 9; dan++) {
    console.log(`--- ${dan}단 ---`);
    for (let i = 1; i <= 9; i++) {
        console.log(`${dan} x ${i} = ${dan * i}`);
    }
}
```

**확장 과제**

- 사용자로부터 단수를 입력받아 해당 단만 출력하도록 만들기

---

### 📌 과제 정리

| 과제명 | 목표 | 활용 문법 |
| --- | --- | --- |
| 계산기 만들기 | 조건문, 연산자 이해 | if, switch, +, -, *, / |
| 구구단 만들기 | 중첩 반복문 훈련 | for, 중첩 루프 |

---

# 3. 자바스크립트 사용자 정의 자료형 활용

- **이론**
    - 객체 리터럴, 생성자 함수
    - 배열과 객체 차이점
    - 구조 분해 할당
- **실습**
    - 간단한 ToDo 리스트를 객체 배열로 구성
    - 사용자 정보 카드 만들기

---

### 1. 객체 리터럴 (Object Literal)

- 객체는 `{ key: value }` 형식으로 정의
- 예:

```jsx
let user = {
  name: "홍길동",
  age: 25,
  email: "hong@test.com"
};

console.log(user.name);  // "홍길동"

```

- 속성 추가/삭제:

```jsx
user.address = "서울";
delete user.age;

```

---

### 2. 생성자 함수 (Constructor Function)

- 유사 클래스를 만들기 위해 사용
- `this`와 `new` 키워드 사용

```jsx
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.sayHello = function() {
    console.log(`안녕하세요, 저는 ${this.name}입니다.`);
  };
}

let p1 = new Person("김범준", 30);
p1.sayHello();

```

---

### 3. 배열과 객체 차이

| 구분 | 배열 | 객체 |
| --- | --- | --- |
| 구조 | 순서 있는 값의 집합 | key-value 형태의 구조 |
| 접근 | index (0, 1, ...) 사용 | 키 이름으로 접근 |
| 용도 | 리스트, 컬렉션 등 | 복잡한 속성의 단일 개체 표현 |

예:

```jsx
let fruits = ["사과", "바나나"];
let car = { brand: "현대", year: 2020 };

```

---

### 4. 구조 분해 할당 (Destructuring Assignment)

```jsx
let user = { name: "Jane", age: 22 };
let { name, age } = user;
console.log(name); // "Jane"

let arr = [1, 2, 3];
let [a, b, c] = arr;
console.log(b); // 2

```

---

### 🧪 실습 과제

### 실습 1: ToDo 리스트 객체 배열 만들기

**목표:** 배열 안에 여러 개의 할 일 항목을 객체로 저장하고 출력하기

```jsx
let todoList = [
  { id: 1, title: "청소하기", done: false },
  { id: 2, title: "공부하기", done: true },
  { id: 3, title: "운동하기", done: false }
];

todoList.forEach((todo) => {
  console.log(`${todo.id}. ${todo.title} [${todo.done ? "완료" : "미완료"}]`);
});

```

**확장 실습 (HTML 출력)**

```html
<div id="todoBox"></div>

<script>
  let html = "<ul>";
  todoList.forEach(todo => {
    html += `<li>${todo.title} - ${todo.done ? "✅" : "❌"}</li>`;
  });
  html += "</ul>";
  document.getElementById("todoBox").innerHTML = html;
</script>

```

---

### 실습 2: 사용자 정보 카드 만들기

**목표:** 사용자 객체 정보를 화면 카드 형식으로 출력

```jsx
let user = {
  name: "김범준",
  age: 35,
  job: "범준샘 AI 아카데미 대표",
  skills: ["HTML", "CSS", "JavaScript"]
};
```

**HTML 출력 예시**

```html
<div id="card"></div>

<script>
let html = `
  <div style="border:1px solid #ccc; padding:10px; width:300px;">
    <h2>${user.name}</h2>
    <p>나이: ${user.age}</p>
    <p>직업: ${user.job}</p>
    <p>기술: ${user.skills.join(", ")}</p>
  </div>
`;
document.getElementById("card").innerHTML = html;
</script>

```

- 전체 소스코드

```html
<!DOCTYPE html>
<html lang="ko">
<head><meta charset="UTF-8"><title>사용자 카드</title>
<style>
#card {
  border:1px solid #ccc; padding:10px; width:300px;
  border-radius: 10px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
</style>
</head>
<body>
<div id="card"></div>
<script>
let user = {
  name: "김범준",
  age: 35,
  job: "범준샘 AI 아카데미 대표",
  skills: ["HTML", "CSS", "JavaScript"]
};
let html = `
  <div>
    <h2>${user.name}</h2>
    <p>나이: ${user.age}</p>
    <p>직업: ${user.job}</p>
    <p>기술: ${user.skills.join(", ")}</p>
  </div>
`;
document.getElementById("card").innerHTML = html;
</script>
</body>
</html>
```

---

### 📌 요약

| 개념 | 실습 예제 |
| --- | --- |
| 객체 리터럴 | 사용자 정보, 할일(ToDo) 객체 |
| 배열 | 여러 개 객체를 리스트로 처리 |
| 구조 분해 | 변수 간편 추출 |

---

### 📝 선택 과제 (심화)

- 사용자 객체를 여러 명 만들어서 배열로 구성하고, 목록을 `<table>`로 출력
- "완료한 할 일"만 필터링해서 보여주는 기능 추가

---

# 4. 자바스크립트 함수

- **이론**
    - 함수 선언문 vs 표현식
    - 매개변수와 return
    - 화살표 함수, 콜백 함수
- **실습**
    - 사칙연산 함수 만들기
    - 버튼 클릭 시 함수 실행

---

### 1. 함수 선언문 vs 함수 표현식

| 구분 | 설명 | 예시 |
| --- | --- | --- |
| **선언문** | 이름 있는 함수 정의, 어디서든 호출 가능 (호이스팅됨) | `function add(x, y) { return x + y; }` |
| **표현식** | 변수에 함수 할당, 호출은 선언 이후에만 가능 | `const add = function(x, y) { return x + y; };` |

```jsx
// 함수 선언문
function greet() {
  console.log("안녕하세요!");
}

// 함수 표현식
const bye = function() {
  console.log("잘가요~");
};

```

---

### 2. 매개변수와 return

```jsx
function add(a, b) {
  return a + b;
}

let result = add(3, 5); // 8

```

- 매개변수: `a`, `b`
- 반환값: `a + b` → 호출 결과로 전달됨

---

### 3. 화살표 함수 (Arrow Function)

```jsx
const multiply = (x, y) => x * y;

const greet = name => console.log(`안녕하세요, ${name}님`);

```

- 간결한 표현 가능
- `this`가 lexical (상위 스코프)으로 바인딩됨

---

### 4. 콜백 함수 (Callback Function)

```jsx
function greetUser(callback) {
  const name = prompt("이름을 입력하세요:");
  callback(name);
}

greetUser(function(name) {
  alert(`환영합니다, ${name}님!`);
});

```

- **콜백 함수**는 다른 함수의 매개변수로 전달되어 나중에 실행되는 함수입니다.

---

### 🧪 실습 과제

### 실습 1: 사칙연산 함수 만들기

**목표:** 사용자로부터 연산자를 받아 해당 연산 수행

```html
<script>
function calculate(x, y, op) {
  switch(op) {
    case '+': return x + y;
    case '-': return x - y;
    case '*': return x * y;
    case '/': return x / y;
    default: return '지원하지 않는 연산자입니다.';
  }
}

let num1 = 10;
let num2 = 5;
let op = '*';

console.log(`결과: ${calculate(num1, num2, op)}`);
</script>

```

**심화:** prompt로 사용자 입력 받기 + 결과 alert 출력

---

### 실습 2: 버튼 클릭 시 함수 실행

**목표:** HTML 버튼 클릭 시 함수 실행하여 결과 보여주기

```html
<button onclick="sayHello()">인사하기</button>

<script>
function sayHello() {
  alert("안녕하세요, 자바스크립트!");
}
</script>

```

---

### ✅ 추가 실습 (선택 과제)

- HTML 입력값 2개와 연산자 select 박스를 만들고, 버튼 클릭 시 결과 출력
- 여러 개의 버튼(+, -, *, /)을 눌러 동적으로 함수 실행

```html
<input type="number" id="num1" value="10">
<input type="number" id="num2" value="2">
<select id="operator">
  <option value="+">+</option>
  <option value="-">-</option>
  <option value="*">*</option>
  <option value="/">/</option>
</select>
<button onclick="doCalc()">계산</button>
<p id="result"></p>

<script>
function doCalc() {
  let n1 = Number(document.getElementById("num1").value);
  let n2 = Number(document.getElementById("num2").value);
  let op = document.getElementById("operator").value;
  let res = calculate(n1, n2, op);
  document.getElementById("result").innerText = "결과: " + res;
}
</script>

```

---

# 5. 자바스크립트 내장 객체

- **이론**
    - String, Number, Array, Date, Math 객체 소개
- **실습**
    - 문자열 처리: 이름 대문자로 바꾸기
    - 배열 정렬, 필터링
    - 현재 시간 표시 프로그램

---

### 1. `String` 객체

- 문자열 처리에 사용되는 내장 객체
- 주요 메서드:
    - `length`, `toUpperCase()`, `toLowerCase()`
    - `indexOf()`, `substring()`, `trim()`, `replace()`

```jsx
let name = " Kim Beomjoon ";
console.log(name.trim().toUpperCase());  // "KIM BEOMJOON"

```

---

### 2. `Number` 객체

- 숫자 관련 메서드 제공
- 주요 기능:
    - `toFixed()`: 소수점 자리수 고정
    - `isNaN()`, `parseInt()`, `parseFloat()`

```jsx
let num = 123.456;
console.log(num.toFixed(1));  // "123.5"

```

---

### 3. `Array` 객체

- 여러 데이터를 순차적으로 저장하는 자료구조
- 주요 메서드:
    - `push()`, `pop()`, `shift()`, `unshift()`
    - `sort()`, `filter()`, `map()`, `forEach()`

```jsx
let nums = [3, 1, 4, 2];
let even = nums.filter(n => n % 2 === 0);
console.log(even);  // [4, 2]

```

---

### 4. `Date` 객체

- 날짜 및 시간 처리
- 주요 메서드:
    - `new Date()`, `getFullYear()`, `getMonth()`, `getDate()`
    - `getHours()`, `getMinutes()`, `getSeconds()`

```jsx
let now = new Date();
console.log(now.getFullYear(), now.getMonth() + 1, now.getDate());

```

---

### 5. `Math` 객체

- 수학 관련 함수 제공 (전역 객체)
- 주요 메서드:
    - `Math.random()`, `Math.floor()`, `Math.ceil()`, `Math.round()`, `Math.max()`, `Math.min()`

```jsx
let r = Math.floor(Math.random() * 10) + 1;  // 1~10 사이 정수

```

---

### 🧪 실습 과제

### 실습 1: 문자열 처리 - 이름 대문자로 바꾸기

```html
<input type="text" id="nameInput" placeholder="이름 입력">
<button onclick="convertName()">대문자로 변환</button>
<p id="result1"></p>

<script>
function convertName() {
  let name = document.getElementById("nameInput").value;
  let upper = name.trim().toUpperCase();
  document.getElementById("result1").innerText = "변환 결과: " + upper;
}
</script>

```

---

### 실습 2: 배열 정렬 및 필터링

```html
<script>
let students = [
  { name: "민준", score: 85 },
  { name: "서연", score: 92 },
  { name: "지후", score: 78 }
];

// 점수 높은 순 정렬
students.sort((a, b) => b.score - a.score);

// 80점 이상 필터링
let passed = students.filter(s => s.score >= 80);

// 출력
passed.forEach(s => console.log(`${s.name}: ${s.score}`));
</script>

```

---

### 실습 3: 현재 시간 표시 프로그램

```html
<p id="clock"></p>

<script>
function updateClock() {
  let now = new Date();
  let hour = now.getHours().toString().padStart(2, '0');
  let min = now.getMinutes().toString().padStart(2, '0');
  let sec = now.getSeconds().toString().padStart(2, '0');
  document.getElementById("clock").innerText = `${hour}:${min}:${sec}`;
}

setInterval(updateClock, 1000);
</script>

```

---

# 6. 브라우저 및 문서 객체

- **이론**
    - window 객체, document 객체
    - DOM 구조 및 접근
    - 요소 선택 및 속성 변경
- **실습**
    - 버튼 클릭 시 배경색 변경
    - 입력된 이름을 화면에 출력

---

### 1. `window` 객체

- 브라우저 창 전체를 의미하는 최상위 객체
- 주요 속성 및 메서드:
    - `alert()`, `prompt()`, `confirm()`
    - `setTimeout()`, `setInterval()`
    - 전역 변수는 자동으로 window 객체의 속성

```jsx
alert("Hello, world!");
console.log(window.innerWidth);  // 창의 가로 길이

```

---

### 2. `document` 객체

- 현재 열려 있는 웹 문서에 접근하는 객체
- HTML 요소 조작의 핵심
- 주요 메서드:
    - `getElementById()`, `getElementsByClassName()`
    - `querySelector()`, `querySelectorAll()`
    - `createElement()`, `appendChild()`

```jsx
let title = document.getElementById("main-title");
console.log(title.innerText);

```

---

### 3. DOM 구조 이해

- DOM(Document Object Model)은 HTML을 트리(Tree) 구조로 표현한 것
- 각 요소(노드)에 접근하거나 조작 가능

```
<html>
  └─ <body>
       └─ <div>
            └─ <p>Hello</p>

```

---

### 4. 요소 선택 및 속성 변경

- `innerText`, `innerHTML`, `value`, `style`, `classList` 등

```jsx
document.getElementById("message").innerText = "안녕하세요!";
document.getElementById("box").style.backgroundColor = "blue";

```

---

### 🧪 실습 과제

### 실습 1: 버튼 클릭 시 배경색 변경

```html
<button onclick="changeBg()">배경색 바꾸기</button>
<div id="box" style="width:200px; height:100px; border:1px solid black;"></div>

<script>
function changeBg() {
  let colors = ["lightblue", "lightgreen", "lavender", "lightyellow"];
  let randomColor = colors[Math.floor(Math.random() * colors.length)];
  document.getElementById("box").style.backgroundColor = randomColor;
}
</script>

```

---

### 실습 2: 입력된 이름을 화면에 출력

```html
<input type="text" id="username" placeholder="이름 입력">
<button onclick="printName()">출력</button>
<p id="output"></p>

<script>
function printName() {
  let name = document.getElementById("username").value;
  document.getElementById("output").innerText = `안녕하세요, ${name}님!`;
}
</script>

```

---

# 7. 자바스크립트 예외처리 및 이벤트 처리

- **이론**
    - try-catch-finally
    - 이벤트 흐름 (버블링 vs 캡처링)
    - 주요 이벤트 종류(onclick, oninput, onsubmit 등)
- **실습**
    - 잘못된 입력 처리하기
    - 클릭 이벤트로 갤러리 이미지 변경

---

### 1. `try-catch-finally` 문

- **오류 처리용 구문**
- 예외 발생 시 프로그램이 멈추지 않고 우회하거나 메시지를 출력하게 함

```jsx
try {
  let json = '{ "age": 25 }';
  let user = JSON.parse(json);
  console.log(user.name.toUpperCase()); // 오류 발생
} catch (err) {
  console.log("오류 발생:", err.message);
} finally {
  console.log("무조건 실행되는 블록입니다.");
}

```

- `try`: 실행할 코드
- `catch`: 오류 발생 시 처리
- `finally`: 오류 여부와 상관없이 항상 실행

---

### 2. 이벤트 흐름 (버블링 vs 캡처링)

- **이벤트 흐름**: 이벤트가 전파되는 과정
    1. **캡처링(Capturing)**: 바깥 → 안쪽
    2. **버블링(Bubbling)**: 안쪽 → 바깥 (기본 동작)

```jsx
document.getElementById("outer").addEventListener("click", () => {
  console.log("바깥 div 클릭");
});

document.getElementById("inner").addEventListener("click", () => {
  console.log("안쪽 div 클릭");
});

```

- 이벤트 리스너의 3번째 인자: `useCapture`
    - `true` → 캡처링
    - `false` → 버블링 (기본값)

---

### 3. 주요 이벤트 종류

| 이벤트 종류 | 설명 |
| --- | --- |
| `onclick` | 클릭 시 발생 |
| `oninput` | 입력 값이 바뀔 때 |
| `onsubmit` | 폼 제출 시 발생 |
| `onchange` | 값이 바뀐 후 포커스를 잃을 때 |
| `onmouseover` / `onmouseout` | 마우스 진입/이탈 시 |

---

### 🧪 실습 과제

### 실습 1: 잘못된 입력 처리하기 (`try-catch` 활용)

```html
<input type="text" id="ageInput" placeholder="나이를 입력하세요">
<button onclick="checkAge()">확인</button>
<p id="msg"></p>

<script>
function checkAge() {
  let age = document.getElementById("ageInput").value;
  try {
    if (isNaN(age)) {
      throw new Error("숫자를 입력해주세요.");
    }
    if (age < 0) {
      throw new Error("나이는 0 이상이어야 합니다.");
    }
    document.getElementById("msg").innerText = `입력한 나이: ${age}`;
  } catch (err) {
    document.getElementById("msg").innerText = `❗ 오류: ${err.message}`;
  } finally {
    document.getElementById("ageInput").value = "";
  }
}
</script>

```

---

### 실습 2: 클릭 이벤트로 갤러리 이미지 변경

```html
<img id="gallery" src="img1.jpg" width="300">
<br>
<button onclick="changeImage('img1.jpg')">1번 이미지</button>
<button onclick="changeImage('img2.jpg')">2번 이미지</button>
<button onclick="changeImage('img3.jpg')">3번 이미지</button>

<script>
function changeImage(filename) {
  document.getElementById("gallery").src = filename;
}
</script>

```

- 이미지 파일은 `img1.jpg`, `img2.jpg`, `img3.jpg` 등으로 준비 필요
- 실제 수업에선 `images/` 폴더와 로컬 이미지 사용

---

# 8. 자바스크립트 API 활용 및 그림판 프로그램 만들기

- **이론**
    - Canvas API 소개
    - getContext(), drawing methods
- **실습**
    - 마우스로 선 그리는 간단한 그림판 만들기
    - 색상/두께 선택 기능 추가

---

### 1. Canvas API란?

- HTML5에서 도입된 2D 그래픽 처리 API
- `<canvas>` 태그를 통해 화면에 직접 그래픽 요소를 그릴 수 있음
- 그림판, 게임, 시각화 도구 등에 사용

```html
<canvas id="myCanvas" width="500" height="400" style="border:1px solid #000;"></canvas>

```

---

### 2. `getContext()` 메서드

- 캔버스에서 2D 그래픽을 그리기 위해 호출하는 메서드

```jsx
let canvas = document.getElementById("myCanvas");
let ctx = canvas.getContext("2d");

```

- `ctx`는 그리기 도구(브러시) 역할

---

### 3. 주요 drawing 메서드

| 메서드 | 설명 |
| --- | --- |
| `moveTo(x, y)` | 펜을 (x, y)로 이동 (선 시작점 지정) |
| `lineTo(x, y)` | (x, y)까지 선을 그림 |
| `stroke()` | 실제로 선을 그림 |
| `beginPath()` | 새로운 경로 시작 |
| `strokeStyle` | 선 색상 설정 |
| `lineWidth` | 선 두께 설정 |

```jsx
ctx.beginPath();
ctx.moveTo(50, 50);
ctx.lineTo(200, 100);
ctx.strokeStyle = "blue";
ctx.lineWidth = 3;
ctx.stroke();

```

---

### 🧪 실습 과제

### 실습 1: 마우스로 선 그리는 간단한 그림판 만들기

```html
<canvas id="canvas" width="500" height="300" style="border:1px solid #333;"></canvas>

<script>
let canvas = document.getElementById("canvas");
let ctx = canvas.getContext("2d");

let drawing = false;

canvas.addEventListener("mousedown", function(e) {
  drawing = true;
  ctx.beginPath();
  ctx.moveTo(e.offsetX, e.offsetY);
});

canvas.addEventListener("mousemove", function(e) {
  if (drawing) {
    ctx.lineTo(e.offsetX, e.offsetY);
    ctx.stroke();
  }
});

canvas.addEventListener("mouseup", function() {
  drawing = false;
});
</script>

```

---

### 실습 2: 색상 및 선 두께 선택 기능 추가

```html
<label>색상: <input type="color" id="colorPicker" value="#000000"></label>
<label>두께: <input type="range" id="lineWidth" min="1" max="10" value="2"></label>

<script>
document.getElementById("colorPicker").addEventListener("change", function() {
  ctx.strokeStyle = this.value;
});

document.getElementById("lineWidth").addEventListener("input", function() {
  ctx.lineWidth = this.value;
});
</script>

```

- 브러시 색상과 굵기를 실시간으로 변경 가능