### 객체

객체: 인덱스로 문자를 사용하는 것

생성 1.

```jsx
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
```

생성 2.

```jsx
var grades = {};
grades['egoing'] = 10;
grades['k8805'] = 6;
grades['sorialgi'] = 80;
```

생성 3.

```jsx
var grades = new Object();
grades['egoing'] = 10;
grades['k8805'] = 6;
grades['sorialgi'] = 80;
```

value값 호출<br> 

`grades['sorialgi']` / `grades.sorialgi`<br> 

객체 안에 객체, 함수도 넣을 수 있음<br> 

### 모듈

- HTML 호출

`<script src="greeting.js"></script>`

- Node.js 호출

`var circle = require('./경로');`

### 정규표현식

정규표현식: 문자열에서 특정한 문자를 찾아내는 도구<br> 

생성 1. 컴파일

```jsx
var pattern = /a/  //1. 리터럴
var pattern = new RegExp('a'); //2. 객체 생성자
```

생성 2. 실행<br> 

`RegExp.exec()`: 패턴을 값으로 하는 배열 리턴, 없으면 null

```jsx
console.log(pattern.exec('abcdef')); // ["a"]
console.log(pattern.exec('bcdefg')); // null
```

`RegExp.test()`: 해당되는 문자열이 있으면 true

```jsx
console.log(pattern.test('abcdef')); // true
cnosole.log(pattern.test('bcdefg')); // false, a 없음
```

`String.match()`: exec와 비슷, 배열 리턴

```jsx
console.log('abcdef'.match(pattern)); // ["a"]
console.log('bcdefg'.match(pattern)); // null
```

`String.replace()`: 패턴을 검색해서 변경 후 변경된 값 리턴

```jsx
console.log('abcdef'.replace(pattern, 'A'));  // Abcdef
//a를 A로 변경
```

옵션<br> 

패턴 뒤에 `i` 를 붙이면 대소문자 구분x

```jsx
var xi = /a/;
console.log("Abcde".match(xi)); // null
var oi = /a/i; //대소문자 구분 x
console.log("Abcde".match(oi)); // ["A"];
```

패턴 뒤에 `g` 를 붙이면 검색된 모든 결과 리턴

```jsx
var xg = /a/;
console.log("abcdea".match(xg));
var og = /a/g;
console.log("abcdea".match(og)); //["a","a"];
```

캡쳐

```jsx
var pattern = /(\w+)\s(\w+)/;
var str = "coding everybody";
var result = str.replace(pattern, "$2, $1");
console.log(result);
```

치환

```jsx
var urlPattern = /\b(?:https?):\/\/[a-z0-9-+&@#\/%?=~_|!:,.;]*/gim;
var content = '생활코딩 : http://opentutorials.org/course/1 입니다. 네이버 : http://naver.com 입니다. ';
var result = content.replace(urlPattern, function(url){
    return '<a href="'+url+'">'+url+'</a>';
});
console.log(result);
```

---

부가 설명 추가 예정....
