## 자바스크립트 기본

### 숫자와 문자

1. 숫자<br>

숫자: 따옴표("")가 붙지 않는 숫자<br>

사칙 연산<br>

```jsx
Math.pow(3,2)= 3^2
.round(x)= x 반올림
.ceil(x) = x 올림
.floor(x) = x 내림
.sqrt(x) = 루트 x
.random(0) = 0~1.0 사이 랜덤 숫자 
	=>round(n*random()): n보다 작은 랜덤 정수
```

2. 문자<br>

문자열(String): 따옴표가(""/ '')가 감싸고 있는 문자 <br>

데이터형 = `typeof.변수` <br>

따옴표를 붙이고 싶을 땐 땐 앞에 `\` = escape <br>

문자열 연산

```jsx
줄바꿈: \n
결합: "문자" + "문자"
문자열 길이: "문자".length
문자 인덱스 : "문자".indexOf("찾는 문자")
```

---

### 변수

선언(생략가능하나 유효 범위 영향 - 권장)<br>

⇒  `var a= a의 값;`<br>

⇒ 중복 선언 `var a=1, b=1;`

변수 : 코드의 재활용성을 높여준다.<br>

변수를 선언하지 않으면 유지보수가 어려움

---

### 주석

 1줄 생략: `//`<br>

여러 줄 생략: `/* */`

---

### 줄바꿈과 여백

생략<br>

---

### 비교

연산자: 값에 대해서 어떤 작업을 지시하기 위한 기호 <br> 

대입연산자`=`

비교연산자<br>

```jsx
`>,>=,<,<=` : 생략

`==` 동등 연산자(equal operator) 
: 서로 같다면 true

`===` 일치 연산자(strict equal operator) 

: '정확'하게 `값과 데이터형` 모두 같을 때 true (권장)

NaN : 특수한 데이터형, 숫자 아님

!=: 같지 않다 ==의 반대

!==: 정확하게 값과 데이터형 모두 같지 않다. ===의 반대
```

var a; // undefined  <br> 

var a=null;  // undefined (의도한 상황) <br> 

```jsx
alert(undefined == null); // undefined
alert(undefined === null); // undefined

alert(true == 1);               //true
alert(true === 1);              //false
alert(true == '1');             //true
alert(true === '1');            //false

alert(0 === -0);                //true
alert(NaN === NaN);             //false
```
