## 자바스크립트 기본

### 조건문

조건문(conditional statement) : 주어진 조건에 따라 다르게 동작학도록 하는 것  <br> 

`if가 true면 코드 실행`,

`if-else 문`,

`if-else if-else문` <br> 

변수와 비교 연산자 <br> 

```jsx
prompt('당신의 나이는?'); //사용자로부터 값을 받음
alert(promt('당신의 나이는?'); //입력받은 값 alert로 발생
```

중첩 조건문<br> 

```jsx
id = prompt('아이디를 입력해주세요.');
        if(id=='egoing'){
            password = prompt('비밀번호를 입력해주세요.');
            if(password==='111111'){
                alert('인증 했습니다.');
            } else {
                alert('인증에 실패 했습니다.');
            }
        } else {
            alert('인증에 실패 했습니다.');
        }
```

논리 연산자 <br> 

`&&` : and, 모두 참일 때 참<br> 

```jsx
id = prompt('아이디를 입력해주세요.');
        password = prompt('비밀번호를 입력해주세요.');
        if(id=='egoing' && password=='111111'){
            alert('인증 했습니다.');
        } else {
            alert('인증에 실패 했습니다.');
        }
```

`||` : or, 둘 중 하나 이상 참이면 참<br> 

```jsx
id = prompt('아이디를 입력해주세요.');
if(id==='egoing' || id==='k8805' || id==='sorialgi'){
    alert('인증 했습니다.');
} else {
    alert('인증에 실패 했습니다.');
} // egoing이거나 k8805이거나 sorialgi이면 인증
```

혼합 사용<br> 

```jsx
id = prompt('아이디를 입력해주세요.');
password = prompt('비밀번호를 입력해주세요.');
if((id==='egoing' || id==='k8805' || id==='sorialgi') && password==='111111'){
    alert('인증 했습니다.');
} else {
    alert('인증에 실패 했습니다.');
} 
//아이디가 egoing이거나 k8805이거나 sorialgi 중 하나여야하고
//패스워드는 111111 이어야 인증
```

`!` not 연산자

```jsx
if(!false && !false){
    alert(4);
}
```

---
boolean의 대체제

```jsx
if(0){ //false
    alert(1)
}
if(1){ //true
    alert(2)
} //0이 아닌 값은 true로 간주
```

false로 간주하는 데이터형

```jsx
if(!''){
    alert('빈 문자열')
}
if(!undefined){
    alert('undefined');
}
var a;
if(!a){
    alert('값이 할당되지 않은 변수'); 
}
if(!null){
    alert('null');
}
if(!NaN){
    alert('NaN');
}
```
