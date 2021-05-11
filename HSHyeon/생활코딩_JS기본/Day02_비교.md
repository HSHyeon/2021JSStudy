## 자바스크립트 기본

### 5. 비교

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
