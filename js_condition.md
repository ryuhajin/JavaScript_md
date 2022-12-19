# 조건문 (Condition)

- 주어진 조건을 만족할 때 코드를 실행하게 하는 문법.

<br>

## if 조건문


- 주어진 조건식이 참이면 if문 블록안에 있는 코드를 실행한다.

``` js
if (조건식) {
    // 조건식이 참이면 이 블록 안의 코드 실행.
}
```
if 조건문 예시

``` js
let a = 10;

if (a === 10) {
    console.log('값이 10이 맞습니다.')
}
```

<br>

## if else문

- if문의 조건식이 참이 아니라 거짓일 경우 실행될 코드.

``` js
if (조건식) {
    // 조건식이 참이면 if문 블록 안의 코드가 실행됨.
} else {
    // 조건식이 거짓이면 else문 블록 안의 코드가 실행됨.
}
```
if else 조건문 예시 

``` js
let a = 70;

if (a === 10) {
    console.log('값이 10이 맞습니다.')
} else {
    console.log('값이 10이 아닙니다.')
} // a의 값이 10이 아니므로 else문 블록 안의 코드가 실행됨.
```

<br>

## else if문

- 조건식이 여러 개인 경우 사용함.

``` js
if (첫번째 조건식) {
    // 첫번째 조건식이 맞으면 이 블록안의 코드 실행.
} else if (두번째 조건식) {
    // 두번째 조건식이 맞으면 이 블록안의 코드 실행.
}
```

조건문 활용 예시

``` js
let age = 25; // 나이 25

if (age >= 65) {
    console.log('free'); // 65세 이상이면 무료
} else if (19 <= age && age <= 64) {
    console.log('$12'); // 19세 이상, 65세 미만이면 12달러 지급
} else {
    console.log('$5'); // 18세 이하면 5달러 지급
}
```

<br>

## switch 문


- 조건식이 여러 개인 경우 사용 가능.
- case 뒤에는 상수만 올 수 있다 ( 숫자 1, 문자열 "hello" 가능 / (a > 10) 불가능)

<br>

``` js
switch () {
    case 상수1:
        // 변수 == 상수1이면 실행.
        break;
    case 상수2:
        // 변수 == 상수2이면 실행.
        break;
    default:
        // 어느 조건(case)에도 해당하지 않는 경우 실행.
}
```
switch 문 사용 예시

``` js
 let drink = "커피"; // 가격을 알고싶은 음료수명

  //switch 조건문
  switch (drink)
  {
    case "콜라" :
      document.write ( "2000원" );
      break;

    case "사이다" :
      document.write ( "1800원");
      break;

    case "커피" :
      document.write ( "2500원" );
      break;

    default :
      document.write ("해당하는 음료수가 존재하지 않습니다.");
  }