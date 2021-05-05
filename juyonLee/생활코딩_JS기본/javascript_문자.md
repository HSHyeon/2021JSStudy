## 생활코딩 - Javascript 내용 정리

### 1. 자바스크립트 기본 

1) 숫자와 문자
데이터는 정보, 종류에 따른 각기 다른 type이 존재한다.
<br>
자바스크립트의 경우, "" 또는 ''로 기본적으로 구별한다.
<br>
기본적으로 문자열(string), 숫자(number)의 형태로 나뉘어진다.

```
alert("3"); //문자 3
alert(3); //숫자 3
alert("hello"); // 문자열
alert(1+1); //숫자 2로 인식 가능.
alert(1.6); //실수도 숫자로 인식함.
```

<br>
관련 함수들 예시

```
Math.pow(3,2); //출력값 9, 3^2
    .round(10.6); //출력값 11, 반올림 연산
    .ceil(10.2); //출력값 11, 올림 연산
    .floor(10.6); //출력값 10, 내림 연산
    .sqrt(9); //출력값 3, 제곱근 연산
    .random(); //0.0~1.0 사이 랜덤한 숫자 출력.

console.log(Math.pow(Math.sqrt(9), 2)); //각 함수들 내부에 인자로 중첩해서 연산 가능.
```

typeof 데이터 : 해당 데이터타입을 알려줌. (string, number)

```
console.log(typeof "1"); //string 출력
console.log(typeof 1); //number 출력
```

 <br>
 '' 또는 ""을 문자열로 변환하여 사용하고 싶은 경우 \(escape)를 이용해 구분자가 아닌 문자로 해석하도록 함.

```
console.log('aa \'bbb\' ccc'); //출력결과 : aa 'bbb' ccc
```

<br>
문자열 더하기 : 숫자의 더하기처럼 +연산자를 이용한다.

```
"aa" + "bb" // "aabb"
"1" + "23" // "123"
```

문자열 길이 구하기 : length함수를 이용한다.
문자열 내에서 특정 문자의 위치 구하기 : indexOf함수를 이용한다.

```
"abcde".length // 출력값 5
"abcde".indexOf(a) // 출력값 0, 해당 값이 없으면 오류가 뜬다.
```
