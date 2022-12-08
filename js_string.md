# 문자열 (String)

- 작은 따옴표(') 와 큰 따옴표(")를 이용하여 정의한다.

``` js
let a = 'hi';
```
a라는 변수에 hi라는 문자열을 할당한 코드.

<br><br>

## 숫자와 구분하기

<br>

``` js
let a = 10; // 숫자 할당
let b = '10'; // 문자열 할당
console.log(a); // 10
console.log(b); // 10
```
<br>

typeof 를 사용하여 변수의 타입을 확인할 수 있지만 아래와 같은 방법으로도 구분이 가능하다.

<br>

``` js
consloe.log(a.length); //undefined
console.log(b.length); // 2
```

- length라는 예약어를 사용하여 타입 구분 가능.
- length는 문자열, 배열의 길이를 숫자 형태로 확인 가능.

## 문자열 안에 변수와 표현식 넣기

- 역 따옴표 (``)(백틱, backtick)을 사용해야 함.
- 큰 따옴표(" "), 작은 따옴표(' ')로는 중간에 표현식을 넣을 수 없음.

역 따옴표 안에 ${변수/표현식}을 넣어주면 문자열 중간에 변수와 표현식 삽입이 가능하다.
``` js
let name = "John";

// 변수를 문자열 중간에 삽입
alert( `Hello, ${name}!` ); // Hello, John!

// 표현식을 문자열 중간에 삽입
alert( `the result is ${1 + 2}` ); // the result is 3
```

<br>

> ### 자바 스트립트에 글자형은 없다.
> 자바 스크립트는 글자(char)형을 지원하지 않는다. 문자(string)형만 존재한다. 문자형에는 글자가 하나 혹은 여러 개 들어갈 수 있다.