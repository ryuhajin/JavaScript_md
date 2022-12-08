# 변수 (Variable)

``` js
let a;
```
a라는 변수를 선언한 코드.

변수를 선언하고 아무 값도 할당하지 않으면 **undefined** 이라는 초기값을 가짐.

<br>

## 변수에 값 할당하기

``` js
let a;
a = 10;
```
- 자바 스크립트는 다른 프로그래밍 언어와 달리 변수의 타입 (int, char 등등) 을 따로 정의하지 않음.
- 코드를 실행할 때 **자동으로 타입이 결정됨.**

<br>

아래와 같이 변수의 값을 바꿀 수 있다.

``` js
let a;
a = 10;
console.log(a); // 10

a = 'hello world'
console.log(a); //hello world

a = false;
console.log(a); //false
```
<br>

## 변수명 규칙

- 영어와 한글 모두 사용 가능.
- 숫자도 사용 가능하나 맨 앞은 숫자로 시작되어선 안됨.
- $, _ 와 같은 특수문자 사용 가능.
- 대소문자가 구분됨.
  
``` js
// 사용 가능한 변수명

let myName;
let 내이름;
let _a;
let $ryu;
```

- 예약어는 사용 불가능함.
> ### 예약어란?  
> 언어에서 미리 지정해놓은 명령어.

``` js
// 사용 불가능한 변수명
let 1myname;
let continue;
let function;
```
<br>

## 변수의 타입 확인하기 - typeof

- 변수에 할당된 값의 타입을 추측하기 어려울 때 **typeof** 라는 예악어로 확인 가능.
  
<br>

``` html
//html

<input value="10" />
```
``` js
// 변수에 input 값 할당

let divEL = document.querySelector('input').value;

// typeof 예약어를 사용하여 divEl의 변수 타입 확인하기

console.log(typeof divEL);
```
<br>

typeof 연산자는 두 가지 형태의 문법을 지원한다.

1. typeof x
2. typeof(x)

괄호가 있든 없든 결과는 동일함.

``` js

typeof undefined // "undefined"

typeof 0 // "number"

typeof 10n // "bigint"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol("id") // "symbol"

```

아래 세 가지 사례는 자세한 설명이 필요하다.

``` js

typeof Math // "object"  (1)

typeof null // "object"  (2)

typeof alert // "function"  (3)

```

1. Math는 수학 연산을 제공하는 내장 객체이므로 "object"가 출력된다.
2. null의 결과는 "object"이지만 null은 **별도의 고유한 자료형을 가지는 특수 값**으로 객체가 아니다. 즉, 언어 자체의 오류이므로 null은 객체가 아님에 유의하자.
3. typeof 는 연산자가 함수면 "function"을 반환한다. 그런데 '함수'형은 따로 없다. 함수는 객체(object)에 속하기 때문이다. 형식적으로 잘못되긴 했지만, 호환성 유지를 위해 남겨진 상태이다. 실무에서는 유용하게 사용되기도 한다.