
# JavaScript 기본 문법

JavaScript는 웹 페이지에서 상호작용을 구현하는 프로그래밍 언어입니다. HTML과 CSS는 웹 페이지의 구조와 스타일을 담당하는 반면, JavaScript는 동적인 동작과 로직을 처리합니다. 자바스크립트는 **객체 지향**, **함수형**, **이벤트 기반** 프로그래밍을 지원하는 다목적 언어입니다.

## 1. JavaScript 기본 문법

JavaScript의 기본 문법은 다음과 같습니다.

### 1.1 변수 선언

JavaScript에서는 **변수**를 선언할 때 `var`, `let`, `const`를 사용합니다. 이들은 변수의 범위(scope)와 재할당 가능 여부에 따라 차이가 있습니다. 

#### **`var`** (예전 방식, 사용 지양)
- `var`는 예전 방식으로, 함수 스코프(function scope)에서만 유효하며 블록 스코프를 지원하지 않습니다.
- **주의**: `var`는 코드에서 예기치 않게 동작할 수 있어 **사용을 지양**하고, **`let`**과 **`const`**를 사용하는 것이 권장됩니다.

#### **`let`** (주로 사용)
- `let`은 ES6에서 도입된 변수 선언 방식으로, **블록 스코프(block scope)**를 지원합니다. 블록 안에서만 유효하고, 같은 이름의 변수를 중복 선언할 수 없습니다.
- **`let`은 주로 사용**되는 방식입니다.

```javascript
let age = 25;  // let으로 변수 선언 (블록 스코프)
```

#### **`const`** (상수 선언)
- `const`는 **상수**를 선언할 때 사용됩니다. **재할당이 불가능**하며, 변수 값을 변경하려고 시도하면 에러가 발생합니다.
- 상수는 한 번 값을 할당하면 **다시 값을 바꿀 수 없**습니다.

```javascript
const PI = 3.14;  // const로 상수 선언 (재할당 불가)
```

```javascript
// 권장하는 변수 선언 방식 예시:
let name = "John";   // 변수는 변경될 수 있어 let 사용
const age = 25;      // 나이는 변경되지 않으므로 const 사용
```

### 1.2 데이터 타입

JavaScript의 기본 데이터 타입은 다음과 같습니다:

- **Primitive(원시) 타입**: String, Number, Boolean, Undefined, Null, Symbol
- **Reference(참조) 타입**: Object (배열, 함수, 객체 등)

#### 1.2.1 원시 데이터 타입

- **String**: 문자열을 나타내는 타입
  ```javascript
  let greeting = "Hello, World!";
  ```

- **Number**: 숫자 타입 (정수 및 실수 모두 포함)
  ```javascript
  let price = 10.5;
  let age = 30;
  ```

- **Boolean**: 참(True) 또는 거짓(False)을 나타내는 타입
  ```javascript
  let isActive = true;
  let isCompleted = false;
  ```

- **Undefined**: 변수 선언은 되었지만 값이 할당되지 않은 상태
  ```javascript
  let user;
  console.log(user);  // undefined
  ```

- **Null**: 명시적으로 값이 없음을 나타내는 타입
  ```javascript
  let person = null;
  ```

#### 1.2.2 참조 데이터 타입

- **Object**: 객체를 나타내는 타입으로, 여러 값을 키-값 형태로 저장할 수 있습니다.
  ```javascript
  let person = {
    name: "John",
    age: 25
  };
  ```

- **Array**: 순서가 있는 데이터 집합을 나타내는 객체입니다.
  ```javascript
  let fruits = ["apple", "banana", "cherry"];
  ```

- **Function**: 특정 작업을 수행하는 코드 블록입니다.
  ```javascript
  function greet() {
    console.log("Hello, World!");
  }
  ```

### 1.3 연산자

JavaScript에서 사용되는 주요 연산자들입니다:

#### 1.3.1 산술 연산자
산술 연산자는 숫자 값을 다룰 때 사용됩니다.

```javascript
let x = 10;
let y = 5;

console.log(x + y); // 덧셈
console.log(x - y); // 뺄셈
console.log(x * y); // 곱셈
console.log(x / y); // 나눗셈
console.log(x % y); // 나머지
```

#### 1.3.2 비교 연산자
비교 연산자는 두 값을 비교하고, 그 결과를 Boolean(true 또는 false) 값으로 반환합니다.

```javascript
let a = 10;
let b = 5;

console.log(a > b);  // true
console.log(a < b);  // false
console.log(a == b); // false (동등 비교)
console.log(a === b); // false (엄격한 동등 비교)
```

#### 1.3.3 논리 연산자
논리 연산자는 주로 조건문에서 사용되며, 두 개 이상의 조건을 결합할 때 사용됩니다.

```javascript
let isActive = true;
let isAdmin = false;

console.log(isActive && isAdmin); // false (AND 연산)
console.log(isActive || isAdmin); // true (OR 연산)
console.log(!isActive);           // false (NOT 연산)
```

### 1.4 조건문

조건문은 주어진 조건에 따라 다른 실행 경로를 결정할 수 있습니다.

#### 1.4.1 if-else 문
```javascript
let age = 20;

if (age >= 18) {
  console.log("성인입니다.");
} else {
  console.log("미성년자입니다.");
}
```

#### 1.4.2 switch 문
```javascript
let day = 2;
let dayName;

switch (day) {
  case 1:
    dayName = "월요일";
    break;
  case 2:
    dayName = "화요일";
    break;
  case 3:
    dayName = "수요일";
    break;
  default:
    dayName = "알 수 없는 요일";
}

console.log(dayName); // 화요일
```

### 1.5 반복문

반복문은 특정 코드를 여러 번 실행할 때 사용됩니다.

#### 1.5.1 for 문
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i); // 0, 1, 2, 3, 4
}
```

#### 1.5.2 while 문
```javascript
let i = 0;
while (i < 5) {
  console.log(i); // 0, 1, 2, 3, 4
  i++;
}
```

### 1.6 함수

함수는 특정 작업을 수행하는 코드 블록입니다. JavaScript에서는 **함수 선언**과 **함수 표현식**을 통해 함수를 정의할 수 있습니다.

#### 1.6.1 함수 선언
```javascript
function greet() {
  console.log("Hello, World!");
}

greet(); // 함수 호출
```

#### 1.6.2 함수 표현식
```javascript
const greet = function() {
  console.log("Hello, World!");
};

greet(); // 함수 호출
```

#### 1.6.3 화살표 함수 (Arrow Function)
ES6에서 도입된 화살표 함수는 코드가 간결해지며, `this`의 동작도 다르게 처리됩니다.

```javascript
const greet = () => {
  console.log("Hello, World!");
};

greet(); // 함수 호출
```

### 1.7 이벤트 처리

JavaScript는 웹 페이지에서 사용자 이벤트를 처리하는 데 사용됩니다. 예를 들어, 버튼 클릭 시 특정 작업을 실행할 수 있습니다.

```javascript
document.getElementById("myButton").addEventListener("click", function() {
  alert("버튼이 클릭되었습니다!");
});
```
