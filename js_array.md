# 배열 (Array)

- 

<br>

## 요소 추가, 제거 메서드

- arr.push(...items) - 맨 끝에 요소 추가.
- arr.pop() - 맨 끝 요소 제거.
- arr.shift() - 맨 앞 요소 제거.
- arr.unshift(...itmes) - 맨 앞에 요소 추가.

## splice

``` js
arr.splice(index, deleteCount, [elem1, ..., elemN])
```
- 첫번째 매개변수 : 조작을 가할 첫 번째 요소를 가리키는 인덱스.
- 두번째 매개변수 : 제거하고자 하는 요소의 개수.
- 이후 매개변수 : 배열에 추가할 요소.

splice 메소드 예시
``` js
let arr = ["I", "study", "JavaScript"];

arr.splice(1, 1); // 인덱스 1부터 시작해 요소 한개 제거

alert(arr); // ["I", "JavsScript"];
```

splice를 사용해 요소를 3개 지우고, 다른 요소 2개로 교체하는 예시
``` js
let arr = ["I", "study", "JavaScript", "right", "now"];

// 0번째 인덱스부터 3번째 까지 요소 지우고 다른 요소로 대체
arr.splice(0, 3, "Let's", "dance")

alert(arr); // ["Let's", "dance", "right", "now"];
```

splice는 **삭제된 요소로 구성된 배열을 반환**한다.
``` js
let arr = ["I", "study", "JavaScript"];

// 처음 두개의 요소를 삭제
let removed = arr.splice(0, 2);

alert( removed ); // ["I", "study"]
```

splice 매서드의 deleteCount를 0으로 설정하면 요소를 제거하지 않고 새로운 요소를 추가할 수 있음.
``` js
let arr = ["I", "study", "JavaScript"];

arr.splice(2, 0, "complex", "language");

alert( arr ); // ["I", "study", "complex", "language", "JavaScript"]
```

## 음수 인덱스 활용
- 배열 관련 메서드에서는 음수 인덱스를 사용할 수 있음.
- 마이너스 부호 앞의 숫자는 배열 끝에서부터 센 요소 위치를 나타냄.

``` js
let arr = [1, 2, 5];

// 인덱스 -1 (배열 끝에서부터 첫 번째 요소)
arr.splice(-1, 0, 3, 4);

alert( arr ); // 1,2,3,4,5
```

## slice
slice 메소드 예시
``` js
arr.slice([start], [end]);
```
- 첫번쨰 매개변수 : 복사를 시작할 인덱스 번호.
- 두번째 매개변수 : (end 인덱스를 제외하고) ~까지 복사할 인덱스 번호.

slice 사용 예시
``` js
let arr = ["t", "e", "s", "t"];

alert( arr.slice(1, 3) ); // e, s

alert ( arr.slice(-2) ); // s, t 
```
- **arr.slice는 서브 배열을 반환한다.**
- arr.slice()로 인수를 하나도 넘기지 않고 arr의 복사본을 만들 수 있다.

## concat

  





