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
