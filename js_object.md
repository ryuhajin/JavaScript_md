# Object

자바 스크립트의 객체는 키(key) : 값(value)으로 구성된 프로퍼티(Property)들의 집합이다.

``` js
let obj = {
    // 각각 key : value.
    color: "red",
    count: 5,

    // 객체는 함수도 가질 수 있음. == 메소드
    log: function () {
        console.log(this.color);
    }

    // 아래와 같이 function 키워드 생략 가능
    log() {
        console.log(this.color);
    }

};
```

<br>

## 속성 추가 / 변경 / 삭제

``` js

// 객체 정의
let obj = {};

obj.num = 10; // num 속성 추가. 숫자 10 할당
```

Object 속성은 대괄호 표기를 사용해 접근할 수도 있다.

- 대괄호 [] 안에 ' '로 감싸주지 않으면 인자로 인식하기 때문에 꼭 감싸주어야 함.

``` js

let obj = {};

obj['num'] = 20; // num 속성 숫자 20 재할당

```

속성 제거는 delete 를 붙여 사용.

``` js

const Employee = {
  firstname: 'John',
  lastname: 'Doe'
};

console.log(Employee.firstname);
// "John"

delete Employee.firstname;

console.log(Employee.firstname);
// undefined

```
<br>

## 속성 (property)

- key의 이름으로는 식별자와 숫자, 문자열 사용 가능.
- 이름이 식별자 형식이 아닐 때는 [''] 형식으로 접근함.

``` js

let x = {
  'a': 1,
  b: 2,
  'a b': 3,
  11: 100
}

x.a // 1
x['a b'] // 식별자 형식이 아닐 때 대괄호 안의 문자열 형식으로 접근.
x[11] // 100

```

기존의 변수를 이용하여 객체를 정의할 수 있음.

``` js

let a = "foo",
  b = 42,
  c = {};

// 단축 프로퍼티 (ES6)
let obj = { a, b, c };

```

속성이 같은 이름을 쓰는 경우, 마지막 값을 사용.

``` js

let a = {x: 1, x: 2};
console.log(a); // {x: 2}

```
<br>

## 객체를 생성하는 방법

### new object()
- object() 생성자 함수를 사용하여 생성.

``` js

//Object()를 이용해서 foo 빈 객체 생성
var foo = new Object();

// foo 객체 프로퍼티 생성 
foo.name = 'foo';
foo.age = 30;
foo.gender = 'male';

console.log(typepf foo); // (출력값) object
console.log(foo); // (출력값) { name: 'foo', age: 30, gender: 'male' }

```

### 객체 리터럴 ({})
- 중괄호를 이용하여 객체 생성.
- {} 안에 아무것도 적지 않은 경우, 빈 객체 생성.

``` js

let Human2 = {
  name: 'john',
  age: '79'
  func1: function () {
		console.log('Hello World')
    }
};

```
### 생성자 함수
- 'new' 연산자와 생성자 함수를 사용하면 유사한 객체를 쉽게 여러개 만들 수 있다.
- 기존 함수에 new 연산자를 붙여서 호출하면 해당 함수는 생성자 함수로 동작함.
- 특정 함수가 생성자 함수로 정의되어 있음 == **함수 이름의 첫 문자를 대문자로 씀.**
  
``` js

// Person() 생성자 함수
var Person = functino(name) {
		this.name = name;
}

// foo 객체 생성
 var foo = new Person('foo');
console.log(foo.name) // foo

```

<br>

## 객체 리터럴 방식와 생성자 함수 방식의 차이점

||객체 리터럴|생성자 함수|
|:---:|:---:|:---:|
|차이점|같은 형태의 객체 재생성 불가.|생성자 함수를 호출할 때, 다른 인자를 넘겨 같은 형태의 객체 생성 가능.|
|생성자 함수|Object()|생성자 함수 자체|

<br>

코드 예시

``` js

// 객체 리터럴 방식으로 foo객체 생성
var foo = {
	name: 'foo',
	age: 35,
	gender: 'man'
}
console.dir(foo);

// 생성자 함수
function Person(name, age, gender, position) {
	this.name = name;
	this.age = age;
	this.gender = gender;
	this.position = position;
}

// Person 생성자 함수를 이용해 bar 객체, baz 객체 생성
var bar = new Person('bar', 33, 'woman')
console.dir(bar)
var baz = new Person('baz', 25, 'woman')
console.dir(baz)

```