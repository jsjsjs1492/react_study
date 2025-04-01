# React 웹 개발 기초 가이드

## 목차
1. [React 소개](#1-react-소개)
2. [컴포넌트 기초](#2-컴포넌트-기초)
3. [JSX 문법](#3-jsx-문법)
4. [상태 관리](#4-상태-관리)
5. [이벤트 처리](#5-이벤트-처리)
6. [데이터 흐름](#6-데이터-흐름)
7. [라우팅](#7-라우팅)
8. [HTTP 요청](#8-http-요청)
9. [스타일링](#9-스타일링)
10. [웹 스토리지](#10-웹-스토리지)
11. [개발 흐름](#11-개발-흐름)

## 1. React 소개

React는 Facebook에서 개발한 JavaScript 라이브러리로, 사용자 인터페이스를 구축하기 위해 설계되었습니다. 컴포넌트 기반 아키텍처를 사용하여 재사용 가능한 UI 요소를 만들 수 있습니다.

### 주요 특징
- **컴포넌트 기반**: UI를 독립적이고 재사용 가능한 조각으로 나눔
- **가상 DOM**: 실제 DOM 조작을 최소화하여 성능 최적화
- **단방향 데이터 흐름**: 예측 가능한 데이터 흐름으로 디버깅 용이
- **선언적 UI**: 상태에 따라 UI가 어떻게 보여야 하는지 선언

## 2. 컴포넌트 기초

React 애플리케이션은 컴포넌트로 구성됩니다. 컴포넌트는 독립적이고 재사용 가능한 코드 조각입니다.

### 함수형 컴포넌트

```jsx
import React from 'react';

const MyComponent = () => {
  return (
    <div>
      <h1>안녕하세요!</h1>
      <p>이것은 함수형 컴포넌트입니다.</p>
    </div>
  );
};

export default MyComponent;

### Props
Props는 부모 컴포넌트에서 자식 컴포넌트로 데이터를 전달하는 방법입니다.
// 부모 컴포넌트
const ParentComponent = () => {
  return <ChildComponent name="홍길동" age={30} />;
};

// 자식 컴포넌트
const ChildComponent = (props) => {
  return (
    <div>
      <p>이름: {props.name}</p>
      <p>나이: {props.age}</p>
    </div>
  );
};

// 구조 분해 할당 사용
const ChildComponent = ({ name, age }) => {
  return (
    <div>
      <p>이름: {name}</p>
      <p>나이: {age}</p>
    </div>
  );
};

## 3. JSX 문법
JSX는 JavaScript XML의 약자로, JavaScript 내에서 HTML과 유사한 마크업을 작성할 수 있게 해주는 문법입니다.

### 기본 규칙
- 항상 하나의 부모 요소로 감싸야 함
- 모든 태그는 닫혀야 함 ( <img /> )
- JavaScript 표현식은 중괄호 {} 안에 작성
- HTML 속성은 camelCase로 작성 (className, onClick)
const element = (
  <div>
    <h1 className="title">안녕하세요</h1>
    <img src={imageUrl} alt="설명" />
    <p>{2 + 2}</p>
  </div>
);

조건부 렌더링
// 삼항 연산자
{isLoggedIn ? <LogoutButton /> : <LoginButton />}

// AND 연산자
{showMessage && <Message />}

// 조건부 함수
{renderContent()}

리스트 렌더링

const items = ['사과', '바나나', '오렌지'];

return (
  <ul>
    {items.map((item, index) => (
      <li key={index}>{item}</li>
    ))}
  </ul>
);

## 4. 상태 관리
상태(State)는 컴포넌트 내에서 변경될 수 있는 데이터입니다.

### useState Hook
```jsx
```

import React, { useState } from 'react';

const Counter = () => {
  // [상태 변수, 상태 변경 함수] = useState(초기값)
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>카운트: {count}</p>
      <button onClick={() => setCount(count + 1)}>증가</button>
      <button onClick={() => setCount(count - 1)}>감소</button>
    </div>
  );
};

### useEffect Hook
컴포넌트의 생명주기와 관련된 작업을 처리합니다

import React, { useState, useEffect } from 'react';

const DataFetcher = () => {
  const [data, setData] = useState([]);
  
  // 컴포넌트가 마운트될 때 실행
  useEffect(() => {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => setData(data));
      
    // 클린업 함수 (언마운트 시 실행)
    return () => {
      console.log('컴포넌트 언마운트');
    };
  }, []); // 빈 배열: 마운트/언마운트 시에만 실행
  
  return (
    <div>
      {data.map(item => (
        <div key={item.id}>{item.name}</div>
      ))}
    </div>
  );
};
