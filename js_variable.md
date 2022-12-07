# 변수 (Variable)

``` js
let a;
```
a라는 변수를 선언한 코드.

변수를 선언하고 아무 값도 할당하지 않으면 **undefined** 이라는 초기값을 가짐.

<br><br>

## 변수에 값 할당하기

<br>

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
<br><br>

## 변수명 규칙

<br>

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

``` js
// 사용 불가능한 변수명
let 1myname;
let continue;
let function;
```
<br><br>

## 변수의 타입 확인하기 - typeof

<br>

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

> ### 예약어란?  
> 언어에서 미리 지정해놓은 명령어.
