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
